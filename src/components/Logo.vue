<template>
  <RouterLink
    to="/"
    class="logo">
    <span>shutopia</span>.MOVIESEARCH
  </RouterLink>
</template>

<style lang="scss" scoped>
@import "~/scss/main";

.logo {
  font-size: 30px;
  font-family: 'Oswald', sans-serif;
  color: black;
  text-decoration: none;
  &:hover {
    color: black;
  }
  span {
    color: $warning;
  }
}
</style>