<template>
  <div id="app">
    <h1 align="center">Retorno de metadados com {{titulo}}</h1>
    <small>
      {{nome}}
    </small>

  </div>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        titulo: 'VueJS!',
        nome: 'Mané Garrincha',
      }
    },
    mounted(){
      setTimeout(()=> this.nome = "Mineirão", 4000)
    }
  }
</script>

<style>


</style>
