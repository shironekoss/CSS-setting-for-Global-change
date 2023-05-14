<template>
<div :class="{ 'dark-mode': isDarkMode }">
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
 <Nestedoverflow/>
</div>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import globalcss from './mycss.css'
import Nestedoverflow from './components/Nestedoverflow'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Nestedoverflow
  },
  computed: {
    isDarkMode() {
      return true
    },
    styles() {
      return this.isDarkMode ? globalcss : 'lightStyles';
    }
  },
   created() {
    this.$options.style = this.styles;
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
