<template>
  <div id="app">
    <h1 v-once v-text="titulo"></h1>
    <div v-if="tarefas.length <= 0"> 
      Não há tarefas
    </div>
    <div v-if ="tarefas.length">
      Existem {{tarefas.length}} tarefas
    </div>

    <div v-if="tarefas.length > 0">
      <ul>
        <li v-for="tarefa in tarefas"> {{tarefa}}</li>
      </ul>
    </div>
    
    <h2>{{subtitulo}}</h2>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      titulo: 'Listagem de tarefas',
      subtitulo: 'Defina uma descrição',
      tarefas: ['Melhorar no HTML','Melhorar no JS', 'Voar com o VueJS']
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: disc;
  padding: 0;
}

li {
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
