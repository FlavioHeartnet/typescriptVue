<template>
  <div id="app">
    <Contador :valorInicial="10"/>
    <ContadorClasse :valorInicial="10"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Contador from './componentes/contatador.vue'
import ContadorClasse from './componentes/contadorClasse.vue'


@Component({
  components: {
    Contador,
    ContadorClasse
  },
})
export default class App extends Vue {}
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
