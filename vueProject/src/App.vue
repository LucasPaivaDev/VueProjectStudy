<template>
  <!-- <theHeader
  v-for="obj in teste"
    v-bind:key="obj.id"
  /> -->

  <div
  v-for="obj in teste"
    v-bind:key="obj.id"
  >
    {{ obj.title }}

  </div>
</template>

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
          "completed": false
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false
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

