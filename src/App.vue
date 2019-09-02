<template>
  <div id="app">
    <div v-show="Slider">
    <img alt="Vue logo" src="./assets/logo.png">
    <Modelo msg="Bem Vindo a Financial Imobiliária."/>
    </div>
    <div>
    <img alt="Vue logo" src="./assets/logo.png">
    <jardim-slider msg="Bem Vindo a Financial Imobiliária."/>
    </div>

  </div>
</template>

<script>
import Modelo from './components/Modelo.vue'
import JardimSlider from './components/JardimSlider.vue'

export default {
  name: 'app',
  Slider: false,
  components: {
    Modelo,
    JardimSlider
  },
  methods:{
   
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #0f6421;
  margin-top: 60px;
}
</style>
