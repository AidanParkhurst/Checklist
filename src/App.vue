<template lang='pug'>
h1 What have you done today?
div(id='taskbar')
  Task(iconPath='src/assets/lifting.png')
  Task(iconPath='src/assets/college.png')
  Task(iconPath='src/assets/MIT.png')
</template>

<script>
import Task from './components/Task.vue'

export default {
  name: 'App',
  components: {
    Task
  }
}
</script>

<style scoped>
#taskbar {
  width: 46%;
  margin: 0 auto;
  overflow: auto;
}
h1 {
  font-family: Helvetica, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 2em;
}
</style>