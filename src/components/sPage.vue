<template>
  <v-ons-page>
    <v-ons-toolbar>
      <div class="left">
        <v-ons-back-button></v-ons-back-button>
      </div>
      
      <div class="center">{{ title }}</div>
      <div class="right">
        <v-ons-toolbar-button>
          <v-ons-icon icon="ion-navicon, material: md-menu"></v-ons-icon>
        </v-ons-toolbar-button>
      </div>
    </v-ons-toolbar>

    <p style="text-align: center">
      <v-ons-button @click="push">
        Hola
      </v-ons-button>
    </p>
  </v-ons-page>
</template>

<script>
import pagina1 from './fPage'
export default {
  name: 'App',
  methods: {
    push(){
      this.$store.commit('navigator/push',pagina1)
    }
  },
  data(){
    return {
        title:"Hola esta es la página 2",
    }
  },
  components: {
    //HelloWorld
  }
  
}
</script>

<style>

</style>