<template>
  <div id="app">
    <index-page></index-page>
  </div>
</template>

<script>
import IndexPage from './components/index'

export default {
  name: 'app',
  components: {
    IndexPage
  }
}
</script>

<style lang="scss">
html, body{
  margin: 0;
  padding: 0;
}
a{
  text-decoration: none;
}
#app {
  font-family: "Source Han Sans CN", "SimSun", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #6f9d5c;
  height: 100%;
  .bg-img{
    background-size: contain;
    background-repeat: no-repeat;
  }
}
</style>
