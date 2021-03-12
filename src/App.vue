<template>
  <v-app>

    <v-app-bar
        color="green"
        height="50px"
    >
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
      <v-toolbar-title>{{componentTitle}}</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer
        temporary
        v-model="drawer"
    >
      <v-list>
        <v-list-item class="px-2">
          <v-list-item-avatar>
            <v-img src="https://randomuser.me/api/portraits/women/85.jpg"></v-img>
          </v-list-item-avatar>
        </v-list-item>

        <v-list-item link>
          <v-list-item-content>
            <v-list-item-title class="title">
              Sandra Adams
            </v-list-item-title>
            <v-list-item-subtitle>sandra_a88@gmail.com</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider></v-divider>

      <v-list
          nav
          dense
      >
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-folder</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Albums</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-account-multiple</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Shared with me</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Starred</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>



    <v-main>

      <v-container fluid>

        <router-view></router-view>
      </v-container>
    </v-main>

  </v-app>

</template>

<script>

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    drawer: false,
    componentTitle: 'App'
  }),
};
</script>
