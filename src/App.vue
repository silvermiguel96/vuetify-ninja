<template>
  <v-app class="grey lighten-4">
    <t-n-navabar></t-n-navabar>
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>

</template>

<script>
import TNNavabar from './components/Navbar.vue'

export default {
  name: 'App',
  components: { TNNavabar },
  data () {
    return {
      //
    }
  }
}
</script>
