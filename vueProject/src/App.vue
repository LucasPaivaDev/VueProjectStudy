<template>
  <!-- <theHeader
  v-for="obj in teste"
    v-bind:key="obj.id"
  /> -->


  <!-- <img src="https://via.placeholder.com/150" alt="teste">   -->

  <div
    v-for="(obj,index) in teste"
    v-bind:key="obj.id"
    class="items"
  >
    <img 
      v-if="obj.imgSrc"
      v-bind:src="obj.imgSrc" 
      alt="teste"
    >

    {{ index }} - {{ obj.title }}

  </div>
</template>

<style>
  .items {
    background: #fff;
    color: #000;
    margin: 0 0 5px 0;
    padding: 3px 6px;

  }

</style>

<script>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import theHeader from './components/theHeader.vue'

export default {
  name: 'App',
  components: {
    theHeader,
    HelloWorld
  },

  data() {
    return {
      
      teste: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false,
          "imgSrc": 'https://via.placeholder.com/150',
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false,
          "imgSrc": 'https://via.placeholder.com/150',

        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
        }
      ]
    }
  }

}

</script>

