<script setup lang="ts">
import { ref } from "vue";
const posts = ref([
  { id: 1, title: "Javascript", body: "Description posts" },
  { id: 2, title: "Python", body: "Description posts" },
  { id: 3, title: "Javascript", body: "Description posts" },
  { id: 4, title: "Javascript", body: "Description posts" },
]);
const createPost=()=>{
  
}
</script>
<template class="App">
  <form class="form">
    <h4>Create post</h4>
    <input class="input" type="text" placeholder="Name" />
    <input class="input" type="text" placeholder="Description" />
    <button class="btn" @click="createPost">Save</button>
  </form>
  <div class="post" v-for="post in posts">
    <div><strong>Name: </strong>{{ post.title }}</div>
    <div><strong>Description:</strong> {{ post.body }}</div>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app{
  padding: 15px;
}
.form{
  display: flex;
  flex-direction: column;
}
.post {
  padding: 15px;
  border: 1px solid teal;
  margin-top: 15px;
}
.input {
  width: 100%;
  border: 1px solid teal;
  padding: 15px;
  margin-top: 15px;
border-radius: 15px;}
.btn {
  padding: 10px;
  border: 1px solid teal;
  background-color: transparent;
  color: black;
  margin-top: 15px;
  align-self: flex-end;
  border-radius: 5px;
}
</style>
