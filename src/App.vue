<template>
  <div id="app">
    <h2>学生信息表：</h2>
    <Students></Students>
    <h2>计数表：</h2>
    <Count></Count>
  </div>
</template>

<script>
import Students from './components/students';
import Count from './components/count';

export default {
  name: 'App',
  components: {
    Students,
    Count
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
