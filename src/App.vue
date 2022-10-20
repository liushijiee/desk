<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <DeskIndex /> 
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import DeskIndex from './components/DeskIndex.vue'
export default {
  name: 'App',
  components: {
    // HelloWorld,
    DeskIndex,
  }
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
