<template>
  <div id="app">
    <h1 v-once v-text="titulo"></h1>
    <div v-if="tarefas.length <= 0">Não há tarefas</div>
    <div v-if="tarefas.length">Existem {{tarefas.length}} tarefas</div>

    <div v-if="tarefas.length > 0">
      <ul>
        <li v-for="tarefa in tarefas">{{tarefa}}</li>
      </ul>
    </div>
    <button v-on:click="tarefas = []">Limpar</button>

    <input v-bind:disabled="tarefas.length == 0" v-model = "subtitulo" type="text" name="" id="">
    
    <h2>{{subtitulo}}</h2>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      titulo: "Listagem de tarefas",
      subtitulo: "Defina uma descrição",
      tarefas: ["Melhorar no HTML", "Melhorar no JS", "Voar com o VueJS"]
    };
  },
  mounted() {
    setTimeout(() => {
      this.titulo = "novo titulo";
      this.tarefas = ["Tarefa 1", "Tarefa 2", "Tarefa 3", "Nova tarefa 1", "Nova tarefa 2", "Nova tarefa 3"];
    }, 3000);
  }
};

</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
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
