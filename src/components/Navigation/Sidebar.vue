<template>
    <v-navigation-drawer v-if="drawer" color="#3A4C72" app>
      <v-img class="pa-4">
        <div class="text-center ml-14" width="100">
            <v-img width="100" src="../../assets/vuebelo logo.png"/>
        </div>
      </v-img>
      <!-- <v-divider/> -->
      <v-list>
        <v-list-item  v-for="[icon, text] in links" :key="icon" link route :to="'/'+ text.toLowerCase()">
          <v-list-item-icon>
            <v-icon class="white--text" >{{ icon }}</v-icon>
          </v-list-item-icon>
  
          <v-list-item-content>
            <v-list-item-title class="white--text" >{{ text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </template>
  
  <script>
  export default {
    name: "SidebarView",
    props: ["drawer"],
    data() {
      return {
        links: [
          ["mdi-microsoft-windows", "Dashboard"],
          ["mdi-account", "Profile"],
          ["mdi-clipboard-list-outline", "Products"],
          ["mdi-card-account-details-outline", "Orders"],
          ["mdi-cog", "System Setting"],
        ],
      };
    },
  };
  </script>
  
  <style scoped></style>
  