<template>
  <v-app dark>
    <v-navigation-drawer v-model="showDrawer" app>
      <v-list>
        <v-list-item v-for="(link,index) in links" :key="index" :to="link.path">
          {{ link.name }}</v-list-items>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar app>
      <v-app-bar-nav-icon @click="showDrawer = !showDrawer" />
      <v-toolbar>
        <v-img src="images/logo.png" max-height="40" max-width="40" contain />
        <v-toolbar-title class="ml-5">
          Stephen Watson
        </v-toolbar-title>
        <v-spacer />
        <v-toolbar-items>
          <v-btn v-for="(link,index) in links" :key="index" :to="link.path">
            {{ link.name }}
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </v-app-bar>
    <v-content>
      <router-view />
    </v-content>
    <v-footer app />
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      showDrawer: false,
      links: [
        { name: 'Home', path: '/' },
        { name: 'Projects', path: '/projects' },
        { name: 'Contact', path: '/contact' }
      ]
    }
  }
}
</script>
