<template>
  <img
    :src="
      `https://assets.coingecko.com/coins/images/12124/large/Curve.png`
    "
    class="d-inline-block v-align-middle line-height-0 circle"
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
