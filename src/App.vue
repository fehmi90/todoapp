<template>
  <div id="app">
    
    <todoApp msg="Welcome to Your Vue.js App"> </todoApp>
  </div>
</template>

<script>
import todoApp from './components/todoApp.vue'

export default {
  name: 'App',
  components: {
    todoApp,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
 
}
</style>
