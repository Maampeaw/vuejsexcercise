<template>
<div>
  <div class="navbar"></div>
  <div id="app">
   <Mydata v-bind:users="users" />
   <!-- <div v-for='user in userss' :key="user.name">
     {{user.name}}
     </div> -->
  </div>
  </div>
</template>

<script>
import Mydata from './components/Mydata.vue'

export default {
  name: 'App',
  components: {
   Mydata
  },
  data(){
    return{
    users: [
      {name:'Papa', color:'green', country:'Ghana', status:'online'},
      {name:'Kwaku', color:'red', country:'Ghana', status:'online'},
      {name:'Ruba', color:'purple', country:'Ghana', status:'online'},
      {name:'David', color:'blue', country:'Ghana', status:'online'},
      {name:'Mike', color:'black', country:'Ghana', status:'online'}
    ]}
  }
}
</script>

<style>
*{
  margin:0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.navbar{
  height: 60px;
  background-image: linear-gradient(to right top, #1a26b2, #b60076, #d33a3b, #c08421, #9bb85a);
}
</style>
