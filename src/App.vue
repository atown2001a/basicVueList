<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <p>{{ newData}}</p>
    <input type="text" v-model="newData" />

    <button @click="onAddNewDataToList" > Add to list</button>
    <ul>
      <li v-for="element in newDataArray" :key="element">{{element}}</li>
   </ul>

  </div>
</template>

<script>


export default {
  name: 'App',

  data () {
    return {
      newData: null,
      newDataArray:[]
    };
  },


  methods:{
    onAddNewDataToList(){
      this.newDataArray.push(this.newData);
      console.log("This list is", this.newDataArray) 
    }
  },


  components: {}
};
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
