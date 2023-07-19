<template>
  <v-container fluid fill-height>
    <v-row align="center" justify="center">
      <v-col cols="12" sm="8" md="4">
        <v-card flat class="elevation-0">
          <v-row align="center" justify="center">
            <v-col cols="auto">
              <v-icon color="#49D9A0" size="35">fab fa-atlassian</v-icon>
            </v-col>
          </v-row>
          <v-card-text>
            <v-form ref="form" @submit.prevent="login">
              <v-text-field
                v-model="username"
                label="Usuário"
                outlined
                color="#49D9A0"
                :rules="[(v) => !!v || 'Campo usuário é obrigatório']"
                required
              ></v-text-field>
              <v-text-field
                v-model="password"
                label="Senha"
                type="password"
                outlined
                color="#49D9A0"
                :rules="[(v) => !!v || 'Campo senha é obrigatório']"
                required
              ></v-text-field>
              <v-btn color="#49D9A0" dark block type="submit">Entrar</v-btn>
            </v-form>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    login() {
      if (this.$refs.form.validate()) {
        // Lógica de autenticação aqui
        console.log("Usuário:", this.username);
        console.log("Senha:", this.password);
      }
    },
  },
};
</script>
