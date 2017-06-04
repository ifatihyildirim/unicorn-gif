<template>
  <div>
    <ul>
    <li v-for="gif in gifs" >
      <img v-bind:src="gif.images.fixed_height.url"  />
    </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['gifs'],
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

ul{
  
}

li{
  list-style: none;
  float: left;
  margin: 20px;
}
</style>
