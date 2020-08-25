<template>
  <button
    :type="type || 'button'"
    @click="$emit('click')"
    class="button"
    :disabled="loading"
  >
    <UiLoading v-if="loading" />
    <slot v-else />
  </button>
</template>

<script>
export default {
  props: {
    loading: Boolean,
    type: String
  }
};
</script>

<style scoped lang="scss">
@import '../../vars';

.button {
  border: none;
  background-color: transparent;
  color: $text;
  border-radius: 0px;
  padding: 4px 12px;
  outline: none;
  height: 26px;
  font-size: 13px;
  font-weight: 600;

  &.button--submit {
    background-color: $curve-blue;
    border: 1px solid $curve-blue;

    &:hover {
      color: $white;
      background-color: $curve-blue;
      border: 1px solid $curve-blue;
    }

    &:disabled {
      color: $white !important;
      border: 1px solid $text-gray;
      background-color: $text-gray;
    }
  }

  &:hover {
    color: $silver-background;
    background: $text-gray;
  }

  &:disabled {
    color: $text-gray !important;
    cursor: not-allowed;
  }
}
</style>
