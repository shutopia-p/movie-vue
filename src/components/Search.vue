<template>
  <div class="container">
    <input
      v-model="title"
      class="form-control"
      placeholder="Search for Movie. series & more." />
    <div class="selects">
      <select
        v-for="filter in filters"
        :key="filter.name"
        class="form-select">
        <option
          v-if="filter.name === 'year'"
          value="All Year">
          All Year
        </option>
        <option
          v-for="item in filter.items"
          :key="item">
          {{ item }}
        </option>
      </select>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      title: '',
      type: 'movie',
      number: 10,
      year: '',
      filters: [
        {
          name: 'type',
          items: ['movie', 'series', 'episode']
        },
        {
          name: 'number',
          items: [10, 20, 30]
        },
        {
          name: 'year',
          items: (() => {
            const years = []
            const thisyear = new Date().getFullYear()

            for (let i = thisyear; i >= 1985; i -= 1) {
              years.push(i)
            }
            return years
          })()
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "~/scss/main";

.container {
  display: flex;
  > * {
    margin-right: 10px;
    &:last-child {
      margin-right: 0;
    }
  }
  .selects {
    display: flex;
    select {
      margin-right: 10px;
      width: 120px;
      &:last-child {
        margin-right: 0;
      }
    }
  }
}
</style>