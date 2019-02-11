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
      <v-btn icon>
          <v-icon right>search</v-icon>
        </v-btn>
    </v-toolbar>
    <v-content>



<v-container
    fluid
    grid-list-lg
    fill-height
    style="height: 434px"
  >
    <v-fade-transition mode="out-in">
      <v-layout v-if="show" key="0" wrap>
        <v-flex xs12>
          <v-card>
            <v-img
              src="https://www.walgreens.com/images/adaptive/sp/920055_Tier2_Household_2600x760.jpg"
              height="434"
              class="grey darken-4"
            ></v-img>
            <!-- <v-card-title class="title">height</v-card-title> -->
          </v-card>
        </v-flex>

      
      </v-layout>

      <v-layout v-else key="1" justify-center>
        <v-btn flat @click="show = true">Load images</v-btn>
      </v-layout>
    </v-fade-transition>
  </v-container>








      <v-card>
        <v-container
          fluid
          grid-list-md
        >
          <v-layout row wrap>
            <v-flex
              v-for="card in cards"
              :key="card.title"
              v-bind="{ [`xs${card.flex}`]: true }"
            >
              <v-card>
                <v-img
                  :src="card.src"
                  height="200px"
                >
                  <v-container
                    fill-height
                    fluid
                    pa-2
                  >
                    <v-layout fill-height>
                      <v-flex xs12 align-end flexbox>
                        <span class="headline white--text" v-text="card.title"></span>
                      </v-flex>
                    </v-layout>
                  </v-container>
                </v-img>

                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn icon>
                    <v-icon>favorite</v-icon>
                  </v-btn>
                  <v-btn icon>
                    <v-icon>bookmark</v-icon>
                  </v-btn>
                  <v-btn icon>
                    <v-icon>share</v-icon>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </v-card>


        </v-layout>
      </v-container>
    </v-content>
    <v-footer app>
      <v-flex
      height="70"
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
      show: true,
       cards: [
        
        { title: 'Dogs Rule', src: 'https://media.npr.org/assets/img/2016/04/29/istock_000068947339_medium_wide-d281af87008ebd62d2862a60d9394f4b37097160-s800-c85.jpg', flex: 6 },
        { title: 'Cat Naps', src: 'https://team-wild.com/wp-content/uploads/2014/07/catnap.jpg', flex: 6  }
      ]
    }),
    props: {
      source: String
    }
  }
</script>
