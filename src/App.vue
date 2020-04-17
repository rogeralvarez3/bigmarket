<template>
  <v-app>
    <v-navigation-drawer app clipped>
      <v-list-item v-for="mn in menu" :key="mn.text" @click="itemClick(mn.text)">
        <v-list-item-icon>
          <v-icon>{{mn.icon}}</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title>{{mn.text}}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-navigation-drawer>
    <v-app-bar app clipped-left>
      <div class="d-flex align-center">
        <v-img
          alt="GranMercado Logo"
          class="shrink mr-2"
          contain
          src="./assets/logo.png"
          transition="scale-transition"
          width="40"
        />

        <h2><strong class="blue--text">Gran</strong><strong>Mercado</strong> </h2>
      </div>
      <v-spacer></v-spacer>
      

      <v-btn text>
        <span class="mr-2">Ingreso</span>
        <v-icon>mdi-lock</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <HelloWorld/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
    menu:[
      {icon:"mdi-cellphone-iphone",text:"Celulares"},
      {icon:"mdi-home-assistant",text:"Para el hogar"},
      {icon:"mdi-laptop-chromebook",text:"Computadoras"},
      {icon:"mdi-wrench",text:"Herramientas"},
      {icon:"mdi-tshirt-v",text:"Ropa"},
      {icon:"mdi-palette",text:"Belleza"},
      {icon:"mdi-cookie",text:"Chucherías"},
      {icon:"mdi-pharmacy",text:"Salud"},
    ]
  }),
  methods: {
    itemClick:function(fn){
      // eslint-disable-next-line no-console
      console.log(fn)
    }
  }
};
</script>
