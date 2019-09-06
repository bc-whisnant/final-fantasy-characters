<template>
  <div id="app">
    <CharacterContainer />
  </div>
</template>

<script>
import CharacterContainer from './components/CharacterContainer.vue'

export default {
  name: 'app',
  components: {
    CharacterContainer
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
  margin-top: 60px;
}
</style>
