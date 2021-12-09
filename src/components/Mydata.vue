<template>
  <div class="data">
      <h2>Users Online</h2>
       
       <div v-for='user in users' :key="user.name" v-show='showUsers'>
           
       <div class="profile">
         <div class="profile-pic" :style='{background: user.color}'>{{user.name.slice(0,2)}}</div>
         <div class="name">{{user.name}}</div>
         <div class="shoesize">{{user.status}}</div>
         <div class="status">{{user.country}}</div>
     </div>


       </div>

       <button v-on:click='toggleShow'><span v-if='showUsers'>Hide users</span><span v-else>Show-users</span></button>
       
  </div>
</template>

<script>
export default {
    name: 'Mydata',
    props: ["users"],
    data(){
        return{
            showUsers : false,
        }
    },
    methods:{
        toggleShow(){
            this.showUsers = !this.showUsers 
        }
    }
}
</script>

<style>
.profile{
    display: flex;
    justify-content: space-evenly;
}
.profile-pic{
    width: 70px;
    height: 70px;
    border-radius: 50%;
    color: white;
    display: flex;
    font-size: 16pt;
    justify-content: center;
    align-items: center;
    font-weight: bolder;
    opacity: 0.7;
}
div{
    margin-bottom: 20px;
}
button{
    width: 100px;
    height: 40px;
    border-radius: 8px;
    background: white;
    color: black

}
button:hover{
    width: 105px;
    height: 45px;
    background: black;
    color: white;
}
h2{
    margin-bottom: 40px;
}

</style>