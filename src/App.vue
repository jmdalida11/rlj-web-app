<template>
  <v-app>
    <v-layout wrap>
      <v-toolbar>
        <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
        <v-toolbar-title class="black--text">RLJ</v-toolbar-title>
        <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>search</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>apps</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>refresh</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>more_vert</v-icon>
        </v-btn>
      </v-toolbar>

    <v-navigation-drawer
          v-model="drawer"
          absolute
          temporary
        >
          <v-list class="pa-1">
            <v-list-tile avatar>
              <v-list-tile-avatar>
                <img src="https://cdn4.vectorstock.com/i/1000x1000/75/48/flat-web-icon-on-white-background-man-programmer-vector-8727548.jpg" >
              </v-list-tile-avatar>

              <v-list-tile-content>
                <v-list-tile-title>John Dalida</v-list-tile-title>
              </v-list-tile-content>
            </v-list-tile>
          </v-list>

          <v-list class="pt-0" dense>
            <v-divider></v-divider>

            <v-list-tile
              v-for="item in items"
              :key="item.title"
            >
              <v-list-tile-action>
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-tile-action>

              <v-list-tile-content>
                <v-list-tile-title><router-link :to="item.link">{{ item.title }}</router-link></v-list-tile-title>
              </v-list-tile-content>
            </v-list-tile>
          </v-list>
      </v-navigation-drawer>
     </v-layout>
    <router-view/>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      drawer: false,
      items: [
        { title: 'Home', icon: 'home', link: '/' },
        { title: 'Register', icon: 'question_answer', link: 'registration' }
      ]
    }
  }
}
</script>

<style>

</style>
