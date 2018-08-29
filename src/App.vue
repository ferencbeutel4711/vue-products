<template>
    <div id="app">
        <content-list :elements="elements"></content-list>
    </div>
</template>

<script>
import ContentList from './components/ContentList.vue';

export default {
  name: 'app',
  components: {
    ContentList,
  },
  data: () => ({
    elements: [
      {
        id: '4711',
        type: 'ProductTile',
        data: {
          id: '4711',
          name: 'Wischmaster4000',
          description: 'Mit diesem Wishmop wird der Boden blitzesauber!',
          imageUrl: 'http://www.vileda.com/media/catalog/product/cache/2/image/800x800/9df78eab33525d08d6e5fb8d27136e95/s/u/supermocio_soft_anwendung.jpg',
          price: '80,00',
        },
      },
      {
        id: '4713',
        type: 'ProductTile',
        data: {
          id: '4713',
          name: 'Mulex Besteck-Set',
          description: 'Das Besteck-Set »ALABAMA« aus dem Hause Mulex verleiht jeder gedeckten Tafel eine elegante Note.',
          imageUrl: 'https://i.otto.de/i/otto/21259151',
          price: '49,99',
        },
      },
    ],
  }),
};
</script>

<style lang="scss">
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
