<template>
 <div class="jumbotron">
  <h1 class="display-3">White Face</h1>
 


   <img src="./assets/88a4068a30ca7f4f1d87b5d1.jpg" alt="Avatar" class="avatar"> 
  <HelloWorld msg="Welcome to Your new you"         />

 <p class="lead">"No more excuses, no delays"</p>
  <hr class="my-2">
  <p>More info</p>
  <p class="lead">
    <a class="btn btn-primary btn-lg" href="Jumbo action link" role="button">Justice Now   </a>
  </p>
</div>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'


 



export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
.avatar {
  vertical-align: middle;
  width: 250px;
  height: 250px;
  border-radius: 50%;
}

.jumbotron{

 background: rgb(32, 32, 32);

}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fafafa;
  background: rgb(32, 32, 32);
  margin-top: 60px;
}
</style>
