<template lang='pug'>
div(id='card' :class='{ completed : isCompleted }')
  img(:src='iconPath' draggable='false' @click='toggleCompleted()')
  figcaption {{ caption }}
</template>

<script>
export default {
  props: {
    iconPath: String,
    caption: String
  },

  data() {
    return {
      isCompleted: false,
    }
  },
  
  methods: {
    toggleCompleted() {
      this.isCompleted = !this.isCompleted;
    }
  }
}
</script>

<style scoped>
img {
  width: 14em;
}
#card {
  background-color: #EEEEEE;
  border: 1px solid #CCCCCC;
  border-radius: 1em;
  box-shadow: 2px 2px 5px grey;
  cursor: pointer;
  float: left;
  margin: 1em;
  text-align: center;
  width: 16em;
}
#card:hover {
  background-color: #DDDDDD;
}

#card.completed {
  background-color: #88D969;
}
#card.completed:hover {
  background-color: #77C858;
}
</style>