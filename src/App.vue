<template>
  <div class="flex-container">

    <the-div v-for="person in people" :key="person.id" :div-text="person.name" :person-id="person.id"></the-div>
  </div>
</template>

<script>
import TheDiv from "@/components/TheDiv";
export default {
  name: 'App',
  components: {TheDiv},
  comments: ['TheDiv'],
  data(){
    return {
      people: [{id: 1, name: 'Uroš'}, {id: 2, name: 'Peđa'}]
    }
  },
}
</script>

<style>

.flex-container {
  display: flex;
}


</style>
