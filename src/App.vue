<template>
  <div id="app">
    <h1>UNICORN GIFS</h1>
    <preview v-bind:gifs=gifs></preview>
  </div>
</template>

<script>
import Preview from './components/Preview.vue'

export default {
  name: 'app',
  components: { Preview },
  data() {
    return {
      gifs: []
    }
  },
  created() {
    fetch('http://api.giphy.com/v1/gifs/search?q=unicorn&api_key=dc6zaTOxFJmzC&limit=50')
    .then((res) => { return res.json() } )
    .then((res) => { this.gifs = res.data; })
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
h1 {
  text-align: center;
}
</style>
