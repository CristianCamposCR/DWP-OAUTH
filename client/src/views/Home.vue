<template>
    <div class="home mt-5">
      <h1 class="text-center">Inicio de sesión con oauth</h1>
      <!-- Revisa la librería se encuentra cargando antes de mostrar los botones de acceso -->
      <div v-if="!$auth.loading" class="d-flex justify-content-center mt-4">
        <!-- muestra el botón de login si no está autentificado -->
        <b-button v-if="!$auth.isAuthenticated" @click="login" variant="primary">Iniciar sesión</b-button>
      </div>
  
    </div>
  </template>
  
  <script>
  export default {
    name: "home",
  
    methods: {
      login() {
        this.$auth.loginWithRedirect();
      },
      logout() {
        this.$auth.logout({
          logoutParams: {
            returnTo: window.location.origin,
          },
        });
      },
    },
  };
  </script>