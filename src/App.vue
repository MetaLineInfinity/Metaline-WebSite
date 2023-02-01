<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import AOS from 'aos'
import 'aos/dist/aos.css'
export default {
  name: 'App',
  mounted () {
    AOS.init()
  }
}
</script>

<style>
* {margin: 0; padding: 0;}
body, html {width: 100%; height: 100%;}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  width: 100%;
  height: 100%;
}

@font-face {
  font-family: 'fzxs';
  src: url("./assets/font/fzxs.otf");
}
</style>
