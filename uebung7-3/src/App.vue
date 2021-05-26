<template>
 <div>Ausgabe Noten</div>
  <div v-for="fach in Noten">{{fach.name}}
    <div v-for="note in fach.grades">{{note}}</div>
  </div>
  <div ></div>
</template>

<script>
export default{
  name:'App',
  data: function (){
    return{
      Noten:[
        {
          name: "Mathematik",
          grades: [5,4.7,3.5,4.1]
        },
        {
          name: "Geschichte",
          grades: [5.5,4.9,5.75]
        },
        {
          name: "Physik",
          grades: [2,2.7,4.3]
        },
        {
          name: "Deutsch",
          grades: [4.25,4.1,3.5]
        },
      ]
    }
    computed:{
      average:function(){

      }
    }

  }

}


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
