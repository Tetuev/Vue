<template>
   <VisitorList/>
</template>

<script>
import VisitorList from './components/VisitorList.vue'

export default {
  name: 'App',
  components: {
    VisitorList
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
