<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      fixed
      app
    >
      <v-list dense>

        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>home</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Home</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>

          <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>search</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Search</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>

        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>pets</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Dogs</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>

        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>pets</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Cats</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>

          <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>shopping_cart</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Products</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>

        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>mail</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Contact</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>

                <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>person</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>User Login</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>

      </v-list>
    </v-navigation-drawer>
    <v-toolbar color="cyan" dark fixed app>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>Adopt-a-Pet</v-toolbar-title>
    </v-toolbar>
    <v-content>

      <v-container fluid fill-height>
        <v-layout
          justify-center
          align-center
        >

          <v-flex text-xs-center>
            <v-tooltip left>
              <v-btn slot="activator" :href="source" icon large target="_blank">
                <v-icon large>code</v-icon>
              </v-btn>
              <span>Source</span>
            </v-tooltip>
            <v-tooltip right>
              <v-btn slot="activator" icon large href="https://codepen.io/johnjleider/pen/rJdVMq" target="_blank">
                <v-icon large>mdi-codepen</v-icon>
              </v-btn>
              <span>Codepen</span>
            </v-tooltip>
          </v-flex>

        </v-layout>
      </v-container>
    </v-content>
    <v-footer app>
      <v-flex
        grey lighten-2
        py-3
        text-xs-center
        black--text
        xs12
      >
      <span class="text-xs-center black--text">&copy; 2019 Adopt-a-Pet&nbsp;  |  &nbsp;Designed by Artistjameshooper.com</span>
          </v-flex>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      drawer: null,
      items: [
          {
            src: 'https://via.placeholder.com/1200x350?text=Visit+Adopt-A-Pet.com+Now'
          },
          {
            src: 'https://via.placeholder.com/1200x350?text=Visit+Adopt-A-Pet.com+Now'
          },
          {
            src: 'https://via.placeholder.com/1200x350?text=Visit+Adopt-A-Pet.com+Now'
          },
          {
            src: 'https://via.placeholder.com/1200x350?text=Visit+Adopt-A-Pet.com+Now'
          }
        ]
    }),
    props: {
      source: String
    }
  }
</script>
