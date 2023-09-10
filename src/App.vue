<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>

  <main>
    <form>
    <div>
     <table>
      <tr>
     <td><label>Name :</label></td>
     <td><input type="text" placeholder="Enter Name" v-model="form.Name"></td>
     </tr>
    <br>
    <tr>
      <td><label>Email :</label></td>
      <td><input type="text" placeholder="Enter Email" v-model="form.Email"></td>
    </tr>
    <br>
    <tr>
      <td><label>Password :</label></td>
      <td><input type="password" placeholder="Enter Password" v-model="form.Password"></td>
    </tr>
    </table>
    <br>
    <button v-on:click="login" type="button" id="log">Login</button> 
    </div>
    </form>
  </main>
</template>

<script>
 export default {
       name:"",
       data()
       {
        return{
          form:{
            Name:'',
            Email:'',
            Password:''
          }
        }
       },
       methods:{
        login(){
          console.warn(this.form)
        }
       }
}
</script>

<style scoped>
*{
  margin: 0;
  
}

#log{
  background: rgb(115, 115, 223);
  border: 0;
  padding: 5px 20px 5px 20px;
}

#log:hover{
    text-decoration: underline;
}
</style>
