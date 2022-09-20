<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <table class="table">
    <!-- <caption>List of users</caption> -->
    <thead>
      <tr>
        <th scope="col">地名</th>
        <th scope="col">描述</th>
        <th scope="col">氣溫</th>
        <th scope="col">降雨機率</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td scope="row">2</td>
        <td>2</td>
        <td>2</td>
        <td>2</td>
      </tr>
    </tbody>
  </table>
  <div id="app">
    <h1>To-Do List</h1>
    {{weather}}
  </div>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// const axios = require('axios'); 
import $ from 'jquery'
//import{onMounted} from 'vue';
// console.log(response.data)
// const url = 'https://192.168.100.139:49157/api/weathers';
const url = 'https://www.google.com.tw/'
export default {
  name: 'App',
  data() {
    return {
      weather: null
    }
  },
  mounted () {
    // axios.get(url).then(response => (this.weather = response))
    $.ajax({
      type: 'GET',
      url: url,
      success: function (result){
        console.log(result)
      }
    });

  },
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
