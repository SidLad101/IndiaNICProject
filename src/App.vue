<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <router-link to="/"><img alt="IndiaNIC" src="./assets/indianic-black-logo.svg" /></router-link>
      </div>

      <v-spacer></v-spacer>

      <router-link to="/">
        <span class="mr-2" style="color:white">Log Out</span>
      </router-link>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
    <v-footer
      color="primary lighten-1"
      padless
    >
      <v-row
        justify="center"
        no-gutters
      >        
        <v-col
          class="primary lighten-2 py-4 text-center white--text"
          cols="12"
        >
          {{ new Date().getFullYear() }} — <strong>IndiaNIC Infotech Limited</strong>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
