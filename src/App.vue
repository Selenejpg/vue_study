<template>
  <div id="app">
    <TestComp/>  
  </div>
</template>

<script>
import "bootstrap"
import TestComp from './components/TestComp.vue'

export default {
  name: 'App',
  components: {
    TestComp
  }
}
</script>

<style lang="scss">
@import "bootstrap/dist/css/bootstrap.min.css";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
