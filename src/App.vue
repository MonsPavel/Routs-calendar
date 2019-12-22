<template>
  <div id="app">
    <CalendarComponent/>
  </div>
</template>

<script>
import CalendarComponent from './components/CalendarComponent.vue'

export default {
  name: 'app',
  components: {
    CalendarComponent
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
