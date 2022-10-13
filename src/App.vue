<template>
  <v-app id="inspire">
    <Sidebar :drawer="drawer" />
    <Topbar @drawerEvent="drawer = !drawer" />
    <v-main style="background: #f5f5f540">
      <v-container class="py-8 px-6" fluid>
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Sidebar from "./components/Navigation/Sidebar.vue";
import Topbar from "./components/Navigation/Topbar.vue";
export default {
  name: "App",
  components: { Topbar, Sidebar },
  data(){
    return {
      cards: ["Today", "Yesterday"],
      drawer: null,
    }
  },
  methods: {},
};
</script>
