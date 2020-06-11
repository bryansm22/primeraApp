<template id="page1">
  <v-ons-page>
    <v-ons-toolbar>
      <div class="left">
      <ons-toolbar-button icon="md-face"></ons-toolbar-button>
    </div>
      <div class="center" >{{ title }}</div>
      <div class="right">
        <v-ons-toolbar-button>
          <v-ons-icon icon="ion-navicon, material: md-menu"></v-ons-icon>
        </v-ons-toolbar-button>
      </div>
    </v-ons-toolbar>

    <p style="text-align: center">
      <v-ons-button @click="push">
        Ir a pagina 2
      </v-ons-button>
    </p>
  </v-ons-page>  
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import pagina2 from './sPage'

export default {
  name: 'App',
  methods: {
    push(){
      this.$store.commit('navigator/push',pagina2)
    }
  },
  data(){
    return {
        title:"Hola esta es la página principal",
        //pageStack: [pagina2]
    }
  },
  components: {
    //HelloWorld
  }
  
}
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
