<template>
  <div id="app" class="p-4">
    
    <Nav-bar />
    <Header title="Item Information" />
    <Item-list />
  </div>
</template>

<script>
import NavBar from './components/NavBar'
import ItemList from './components/ItemList.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    ItemList,
    Header
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
  background-color:#FAFAFA;
  margin-top: 60px;
}
</style>
