<template>
  <svg :width="size" :height="size" viewBox="0 0 100 100">
    <path
      fill="none"
      stroke="currentColor"
      stroke-width="10"
      d="M30,30C30,14.31 44.31,0 60,0C75.69,0 90,14.31 90,30C90,45.69 75.69,60 60,60C44.31,60 30,45.69 30,30ZM60,30C73.24,30 84,40.76 84,53C84,65.24 73.24,76 60,76C46.76,76 36,65.24 36,53C36,40.76 46.76,30 60,30Z"
    />
  </svg>
</template>

<script>
export default {
  props: {
    size: {
      type: Number,
      default: 100,
    },
  },
};
</script>

<style scoped>
</style>
