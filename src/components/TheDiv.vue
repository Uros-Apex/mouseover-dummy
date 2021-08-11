<template>
  <div @mouseover="setNewText(personId)" @mouseleave="setDefaultText(personId)" class="flex-child magenta" style="height: 400px">
    {{ divText }}
  </div>

</template>

<script>
export default {
  name: "TheDiv",
  props: ['divText', 'personId'],
  methods: {
    setNewText(id){
      if(id === 1){
        this.divText = 'Uroš se menja na mouseover i na mouseleave!'
      }else{
        this.divText = 'Peđa se menja na mouseover i na mouseleave!'
      }
    },
    setDefaultText(id){
      if(id === 1){
        this.divText = 'Uroš'
      }else{
        this.divText = 'Peđa'
      }
    }
  }
}
</script>

<style scoped>
.flex-child {
  flex: 1;
  border: 2px solid yellow;
}

.flex-child:first-child {
  margin-right: 20px;
}
</style>