<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>Have been added {{itemList.length}} items.</h1>
    <input type="text" v-model="newItem" placeholder="Add item.." />
    <button @click="addItem">
      Add
    </button>
    <ItemComponent v-for="(item, index) in itemList" 
    :element="item" :key="index" />
  </div>
</template>

<script>
import ItemComponent from './components/ItemComponent.vue'


export default {
  name: 'App',
  components: {
    ItemComponent
  },
  data() {
    return {
      newItem: "",
      itemList: []
    }
  },
  methods: {
    addItem: function() {
      this.itemList.push(this.newItem);
      this.newItem = "";
    }
  }
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
