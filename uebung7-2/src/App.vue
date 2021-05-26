<template>
  <div class="content">Test</div>
  {{myString}}
  <input type="text" value="{{myString}}">
  <ul>
    <li v-for="todo in todos ">{{todo}}</li>
  </ul>
  <input v-model="newTodo">
  <input v-model="" >
  <button v-on:click="addTodo()">Add Something</button>
</template>

<script>
  export default {
    name: 'App',
    data: function () {
      return {
        myString: 'Hello World2',
        todos: [
          'Sachen kaufen',
          'Sache passieret',
          'Raoul',
        ],
        newTodo: ''
      }},

      methods: {
        addTodo: function () {
          this.todos.push({
            name: this.newTodo,
            time: parseInt(this.newTime)
          });
          this.newTodo = "";
          this.newTime = 0;
        }
      },
      computed:{
      todoCount: function(){
        return this.todos.length;
      },
      totalTime:function(){
        var time =0;

        this.todos.forEach(function (todo){
          time += todo.time;
        })
        return  time;
      }}}

</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
