<template>
<!-- 
  Template Ref

  Template ref allows us to store a refernce to a raw DOM element inside
  of a variable, then we can use regualr JS mehthods and properties
  on it to change its text content, styles ect...
  Since we will have hold of a normal DOM element, this means
  that we have access to all of the normal DOM API

  the element that we get, is the same as if we were to use a query selector in JS

  NOTE: this.$refs will give us access to all the refs
 -->
  <h1>{{ title }}</h1>
  <input type="text" ref="name">
  <button v-on:click="handleClick">Click Me!</button>
</template>

<script>

export default {
  name: 'App',
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
