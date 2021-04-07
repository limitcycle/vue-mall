<template>
  <v-app-bar color="rgb(250, 250, 250)" app>
    <!-- <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon> -->

    <v-app-bar-title>
      v-toolbar-title
      <!-- Application -->
    </v-app-bar-title>

    <v-spacer></v-spacer>

    <v-btn text x-large to="/login">
      登入
    </v-btn>

    <v-btn text x-large>
      <v-icon>mdi-cart</v-icon>
    </v-btn>

    <v-btn text x-large>
      <v-icon>mdi-magnify</v-icon>
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: 'Header'
}
</script>
