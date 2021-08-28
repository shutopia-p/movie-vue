<template>
  <Headline />
  <Search />
</template>

<script>
import Headline from '~/components/Headline'
import Search from '~/components/Search'

export default {
  components: {
    Headline,
    Search
  }
}
</script>

<style lang="scss" scoped>
@import "~/scss/main";
</style>