<template>
  <v-ons-page>
    <v-ons-toolbar>
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
  data(){
    return {
        title:"Hola esta es la página 2",
        pageStack: [pagina1]
    }
  },
  components: {
    //HelloWorld
  }
  
}
</script>

<style>

</style>