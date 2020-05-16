<template>
  <div>
    <h1>To Dos</h1>
    <p  v-on:click='e=>toggleClass(e)'  v-for='todo in todos' :key="todo">{{todo}}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return{
      todos: ['feed the cat', 'clean my room'],
      isHidden: false
    }
  },
  methods:{
    toggleClass(e){
      return e.target.classList.toggle('hide')
    }
  }
}
</script>

<style scoped>
.hide{
  color: blue;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
