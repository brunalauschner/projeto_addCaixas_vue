<template>
  <div id="app">
    <toDoForm :caixinhas="caixinhas" @addCaixa="addCaixa($event)"/>
    <toDoList :caixinhas="caixinhas"/>
  </div>
</template>

<script>
import toDoForm from "./components/ToDoForm.vue"
import toDoList from "./components/ToDoList.vue"

export default {
  name: 'App',
  components: {
    toDoForm, toDoList
  }, 
  data: function() {
    return{
      caixinhas: [{
        titulo: "Estudar"
      },{
        titulo: "Jogar"
      }
      ]
    }
  }, methods:{
    addCaixa: function(event){
      this.caixinhas.push({titulo: event.titulo})
    }
    }
  }
</script>

<style>
</style>
