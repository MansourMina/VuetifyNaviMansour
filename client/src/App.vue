<template>
  <v-app>
    <!-- Aufgabe 2 -->
    <!-- <v-app-bar class="grey lighten-5" height="74" app>
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
    </v-main> -->

    <!-- Aufgabe 3 -->
    <!-- <v-app-bar class="blue" app>
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
        class="white--text"
      ></v-app-bar-nav-icon>
      <span class="white--text title">Layout Demo</span>
    </v-app-bar>
    <v-navigation-drawer
      app
      hide-overlay
      disable-resize-watcher
      v-model="drawer"
    >
      <v-row>
        <v-col cols="6">
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="text-h6">
                Menu
              </v-list-item-title>
              <v-list-item-subtitle>
                Please select
              </v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col cols="6">
          <v-btn text @click="drawer = false" float="right" class="mt-4"
            >Close</v-btn
          >
        </v-col>
      </v-row>

      <v-divider></v-divider>
      <v-list-item-group active-class="blue white--text">
        <v-list-item
          link
          v-for="(route, i) in routes"
          :key="i"
          :to="route.link"
        >
          {{ route.name }}
        </v-list-item>
      </v-list-item-group>
    </v-navigation-drawer> -->

    <!-- Aufgabe 4 -->
    <v-app-bar class="blue" app>
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
      <div class="hidden-md-and-down">
        <v-btn
          active-class="white--text orange"
          class="white--text black"
          to="/"
          exact
          >Home</v-btn
        >
        <v-btn
          active-class="white--text orange"
          class="white--text black ml-5"
          to="/products"
          
          >Products</v-btn
        >
        <v-btn
          active-class="white--text orange"
          class="white--text black ml-5"
          to="/about"
          exact
          >About</v-btn
        >
      </div>

      <v-app-bar-nav-icon
        v-if="!drawer"
        @click.stop="drawer = !drawer"
        class="white--text hidden-lg-and-up"
      ></v-app-bar-nav-icon>
    </v-app-bar>

    <v-navigation-drawer
      app
      hide-overlay
      disable-resize-watcher
      v-model="drawer"
      right
    >
      <v-row>
        <v-col cols="6">
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="text-h6">
                Menu
              </v-list-item-title>
              <v-list-item-subtitle>
                Please select
              </v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col cols="6">
          <v-btn text @click="drawer = false" float="right" class="mt-4"
            >Close</v-btn
          >
        </v-col>
      </v-row>

      <v-divider></v-divider>
      <v-list-item-group active-class="blue white--text">
        <v-list-item
          link
          v-for="(route, i) in routes"
          :key="i"
          :to="route.link"
        >
          {{ route.name }}
        </v-list-item>
      </v-list-item-group>
    </v-navigation-drawer>

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
    routes: [
      { link: '/', name: 'Home' },
      { link: '/products', name: 'Products' },
      { link: '/team', name: 'Team' },
      { link: '/about', name: 'About' },
    ],

    drawer: false,
  }),
  methods: {
    isMobile() {
      if (
        /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(
          navigator.userAgent,
        )
      ) {
        return true;
      } else {
        return false;
      }
    },
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap');
a:not(active-class) {
  color: grey !important;
}
</style>
