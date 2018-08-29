<template>
    <div class="product-tile" v-on:click="toggleExtension">
        <p>{{data.name}}</p>
        <img class="product-tile__image" :src="data.imageUrl"/>
        <p>{{data.description}}</p>
        <p>Only {{data.price}}$</p>
    </div>
</template>

<script>
export default {
  name: 'ProductTile',
  props: {
    data: {
      type: Object,
      required: true,
    },
  },
  data: () => ({
    extended: false,
  }),
  methods: {
    toggleExtension() {
      const extendedClass = 'product-tile--extended';
      if (this.extended) {
        this.$el.classList.remove(extendedClass);
        this.extended = false;
      } else {
        this.$el.classList.add(extendedClass);
        this.extended = true;
      }
    },
  },
};
</script>

<style scoped lang="scss">
    .product-tile {
        display: inline-block;
        height: 400px;
        width: 300px;
        border: 1px solid;
        overflow: hidden;
        background-color: #d4d4d4;

        &:nth-child(even) {
            margin-left: 8px;
        }

        &:nth-child(odd) {
            margin-right: 8px;
        }

        &--extended {
            height: 500px;
        }

        &__image {
            max-width: 100%;
            max-height: 300px;
        }
    }
</style>
