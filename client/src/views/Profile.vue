<template>
  <div class="vh-100 d-flex align-items-center justify-content-center">
    <b-row >
      <b-col cols="12" sm="12">
        <b-card no-body class="overflow-hidden" style="max-width: 600px">
          <b-row no-gutters>
            <b-col md="6">
              <b-card-img
                :src="$auth.user.picture"
                alt="Image"
                class="rounded-0"
              ></b-card-img>
            </b-col>
            <b-col md="6">
              <b-card-body :title="$auth.user.name">
                <div><strong>Nombres:</strong> {{ $auth.user.given_name }}</div>
                <div>
                  <strong>Apellidos:</strong> {{ $auth.user.family_name }}
                </div>
                <div>
                  <strong>Nombre de usuario:</strong> {{ $auth.user.nickname }}
                </div>
                <div><strong>Correo:</strong> {{ $auth.user.email }}</div>
              </b-card-body>
            </b-col>
          </b-row>
        </b-card>
      </b-col>
    </b-row>
  </div>
</template>
