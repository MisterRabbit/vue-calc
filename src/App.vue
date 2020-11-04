<template>
  <div id="app">
    <Calculate/>
  </div>
</template>

<script>
import Calculate from '@/components/Calculate.vue'

export default {
  name: 'App',
  components: {
    Calculate
  },
  methods: {

  }
}
</script>

<style src="@/assets/styles/reset.css"></style>
<style>
* {
  font-family: 'Gilroy',sans-serif;
  transition: 0.3s all;
    font-weight: 600;
}
body {
  display: flex;
  height: 100vh;
  justify-content: center;
  align-items: center;
  background: rgb(30 30 30);
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 200px;
  box-shadow: 0 3px 15px grey;
}
</style>
