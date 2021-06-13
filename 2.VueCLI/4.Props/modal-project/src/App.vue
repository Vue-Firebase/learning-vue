<template>
  <h1>{{ title }}</h1>
  <input type="text" ref="name">
  <button v-on:click="handleClick">Click Me!</button>
  <Modal />
</template>

<script>
// bring in the new component
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  // register imported components
  components: {
    Modal
  },
  data() {
    return {
      title: 'My First Vue CLI App'
    }
  },
  methods: {
    handleClick() {
      // use the ref here
      this.$refs.name.value = "Hello"
    }
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
