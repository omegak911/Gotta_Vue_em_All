<template>
  <div>
    <Menu />
    <nuxt />
  </div>
</template>

<script>
import Menu from '../components/Menu';
import { store } from '../store/store.js';

export default {
  components: {
    Menu
  },  
  store,
  beforeMount: function() {
    this.$store.commit('fetchAllPokemon');
  },
}
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}

.page {
  height: 95vh;
}

.flexCenter {
  display: flex;
  justify-content: center;
  align-items: center;
}

.flexColumn {
  flex-direction: column;
}

</style>