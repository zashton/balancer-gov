<template>
  <img
    src="~/@/assets/Keep3r-logo.svg"
    class="d-inline-block v-align-middle line-height-0"
    :style="{
      width: `${size || 22}px`,
      height: `${size || 22}px`
    }"
  />
</template>

<script>
export default {
  props: ['address', 'size']
};
</script>
