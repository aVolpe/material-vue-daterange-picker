<template>
    <v-text-field v-model="value" :label="title" readonly />
</template>

<script>
export default {
  inheritAttrs: false,
  inject: ['picker'],
  props: ['value', 'title'],
  computed: {
    inputClass () {
      return {
        'text-field__filled': this.value.trim().length > 0,
      };
    },
  },
};
</script>


<style lang="scss">
@import '../../styles/components/activator.scss';
</style>
