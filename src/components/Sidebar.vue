<template>
  <v-card width="256" class="mx-0 sidebar">
    <v-navigation-drawer permanent>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6"> Номенклатура </v-list-item-title>
          <v-list-item-subtitle> </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
            <v-list-item v-for="item in items" :key="item.title" link>
              <v-list-item-icon>
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-card>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "Sidebar",

  data() {
    return {
      items: [
        { title: "Главная", icon: "folder_open" },
        { title: "Память", icon: "folder_open" },
        { title: "Мониторы", icon: "folder_open" },
        { title: "Коммутаторы", icon: "folder_open" },
        { title: "Аксессуары", icon: "folder_open" },
      ],
    };
  },
});
</script>
