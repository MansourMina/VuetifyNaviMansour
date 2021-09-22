<template>
  <v-app>
    <v-app-bar class="grey lighten-5" height="74" app>
      <img
        class="mx-2"
        src="@/assets/tesla-motors-1.svg"
        style="height:150px; margin-top:100px"
      />
      <span
        class="text-truncate text-h4 blue-grey--text darken-1"
        style="font-family: Poppins"
        >Tesla Inc.</span
      >
      <v-spacer></v-spacer>
      <v-btn active-class="white--text orange" class="white--text black" to="/" exact>Home</v-btn>
      <v-btn active-class="white--text orange" class="white--text black ml-5" to="/products" exact 
        >Products</v-btn
      >
      <v-btn active-class="white--text orange" class="white--text black ml-5" to="/about" exact 
        >About</v-btn
      >
    </v-app-bar>
    <v-main>
      <div class="d-flex">
        <div style="width:250px"></div>
        <div class="mt-10" style="flex:1"><router-view></router-view></div>
      </div>
    </v-main>
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

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap');
a:not(active-class) {
  color: grey !important;
}
</style>
