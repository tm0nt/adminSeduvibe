<template>
  <v-navigation-drawer app color="white" right width="290">
    <v-toolbar color="rgba(0,0,0,0)" flat>
      <v-toolbar-title>Central</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn rounded small>Ver tudo</v-btn>
    </v-toolbar>
    <v-list subheader two-line class="mt-n4">
      <v-list-item v-for="file in files" :key="file.title">
        <v-list-item-avatar>
          <v-icon :class="file.color" dark>{{ file.icon }}</v-icon>
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title>{{ file.title }}</v-list-item-title>
          <v-list-item-subtitle>{{ file.subtitle }}</v-list-item-subtitle>
        </v-list-item-content>
        <v-list-item-action>
          <v-btn icon>
            <v-icon color="grey lighten-1" small>fas fa-ellipsis-h</v-icon>
          </v-btn>
        </v-list-item-action>
      </v-list-item>
    </v-list>
    <v-toolbar color="rgba(0,0,0,0)" flat class="mt-n6">
      <v-toolbar-title>Projetos</v-toolbar-title>
    </v-toolbar>
    <v-card class="mx-2 rounded-l-xl pb-1" flat color="#EEEEEE">
      <v-row>
        <v-col cols="12" sm="8">
          <v-list-item two-line class="mt-n4">
            <v-list-item-content>
              <v-list-item-title>Vídeochamadas</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col cols="12" sm="4">
          <v-progress-circular
            :size="50"
            :width="3"
            :value="75"
            color="teal"
            class="ml-n5 mt-n1"
          >
            75
          </v-progress-circular>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="mx-2 rounded-l-xl pb-1 mt-5" flat color="#EEEEEE">
      <v-row>
        <v-col cols="12" sm="8">
          <v-list-item two-line class="mt-n4">
            <v-list-item-content>
              <v-list-item-title>VibePlus</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col cols="12" sm="4">
          <v-progress-circular
            :size="50"
            :width="3"
            :value="42"
            color="teal"
            class="ml-n5 mt-n1"
          >
            42
          </v-progress-circular>
        </v-col>
      </v-row>
    </v-card>

    <div class="mt-2 mx-2">
      <v-btn rounded small block>Ver mais</v-btn>
    </div>
  </v-navigation-drawer>
</template>

<script>
export default {
  data() {
    return {
      files: [
        {
          color: "green",
          icon: "fas fa-mobile",
          subtitle: "On-line",
          title: "Aplicação",
        },
        {
          color: "red",
          icon: "fas fa-address-card",
          subtitle: "A alterar",
          title: "Endereços",
        },
        {
          icon: "fas fa-user-shield",
          color: "orange",
          subtitle: "Online",
          title: "Admin Painel",
        },
        {
          color: "purple",
          icon: "fas fa-credit-card",
          subtitle: "Online",
          title: "Gateway",
        },
        {
          color: "blue",
          icon: "fas fa-address-card",
          subtitle: "Offline",
          title: "KYC",
        },
      ],
    };
  },
};
</script>

<style></style>
