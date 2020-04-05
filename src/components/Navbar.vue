<template>
  <nav>

    <v-toolbar flat app>
     
      <v-toolbar-title class="text-uppercase grey--text">
        <span class="font-weight-light">Project</span>
        <span>Name</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>

      <!-- dropdown menu -->
   <v-menu offset-y>
    <template v-slot:activator="{ on }">
        <v-btn text v-on="on" color="grey" class="text--darken-2">
            <v-icon left>mdi-chevron-down</v-icon>
            <span>Menu</span>
        </v-btn>
    </template>
        <v-list>
            <v-list-item
                v-for="(link,idx) in links"
                :key="idx"
                :to="link.route"
            >
          <v-list-item-title>{{ link.text }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
      <v-btn flat color="grey">
        <span>Sign Out</span>
        <v-icon right>exit_to_app</v-icon>
      </v-btn>
    </v-toolbar>

    

  </nav>
</template>
    <!-- <v-navigation-drawer app v-model="drawer" class="primary">
      <v-layout column align-center>
        <v-flex class="mt-5">
          <v-avatar size="100">
            <img class="text-lg-center" src="/character-1.jpg">
          </v-avatar>
          <p class="white--text subheading mt-1">The Net Ninja</p>
        </v-flex>
      </v-layout>
      <v-list>
        <v-list-tile v-for="link in links" :key="link.text" router :to="link.route">
          <v-list-tile-action>
            <v-icon class="white--text">{{ link.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title class="white--text">{{ link.text }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer> -->

<script>
export default {
  components:{

  },
  data() {
    return {
      
      // drawer: null,
      links: [
        { icon: 'dashboard', text: 'Home', route: '/' },
        // { icon: 'folder', text: 'Sign In', route: '/Home' },
        { icon: 'person', text: 'About', route: '/about' },
      ]
    }
  }
}
</script>
