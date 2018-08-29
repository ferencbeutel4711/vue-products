<template>
    <div class="content-list">
        <component v-for="element in elements" :is="element.type" :data="element.data" :key="element.id"></component>
    </div>
</template>

<script>
import ProductTile from './ProductTile.vue';

export default {
  name: 'ProductList',
  components: { ProductTile },
  props: {
    elements: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped lang="scss">
    .content-list {
        width: 100%;
        padding: 8px;
        margin: 0 auto;
        max-width: 768px;
    }
</style>
