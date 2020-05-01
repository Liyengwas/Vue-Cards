<template>
  <main id="app">
   <section class="products">
    
     <Product 
      v-for="product in products"
      :key="product.color"
      :product="product"
     />

   </section>
  </main>
</template>

<script>

import Product from './components/Product';

export default {
  name: 'App',
  components: {
    Product
  },

  data () {
    return {
      products : [
        {
          title: 'Nissan R32',
          color: 'black',
          bgtext: 'R32',
          src: require('./assets/r32.jpg') 
        },
        {
          title: 'Nissan R33',
          color: 'black',
          bgtext: 'R33',
          src: require('./assets/r33.jpg') 
        },
        {
          title: 'Nissan R34',
          color: 'blue',
          bgtext: 'R34',
          src: require('./assets/r34.jpg') 
        }
        // {
        //   title: 'Nissan R35',
        //   color: 'white',
        //   bgtext: 'R35',
        //   src: require('./assets/r35.jpg') 
        // }
      ]
    }
  }
}
</script>

<style>
  
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body{
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main{
    width: 100vw;
    min-height: 100vh;
    overflow: hidden;

    background-color: #EEE;
    display: flex;
    align-items: center;
  }

  .products{
    display: flex;
    max-width: 1280px;
    padding: 25px;
    margin: 0 auto;
  }
</style>
