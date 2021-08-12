<template>
  <v-app>
    <v-content class="fondo">
      <v-container class="fill-height" fluid>
        <v-row aling="center" justify="center">
          <v-col cols="12" sm="8" md="8">
            <v-card class="elevation-12">
              <v-window class="contenedor">
                <v-row class="d-flex">
                  <v-col
                    class="
                      d-flex
                      flex-column
                      align-end
                      justify-space-around
                      order-2
                    "
                    cols="12"
                    sm="12"
                    md="6"
                    lg="6"
                  >
                    <img
                      class="imagen"
                      src="medicina.svg"
                    />
                  </v-col>
                  <v-col cols="12" sm="12" md="6" lg="6">
                    <v-card-text
                      class="d-flex flex-column justify-space-around"
                    >
                      <h2
                        class="
                          text-center
                          display-2
                         secondary--text 
                          text--secondary-3
                          mb-5
                        "
                      >
                        Consultar Lugar de Vacunacion
                      </h2>

                      <v-form>
                        <v-text-field
                          label="Cédula"
                          name="cedula"
                          v-model="cedula"
                          type="text"
                          color="secondary"
                        />
                        <v-text-field
                          id="Fecha de Nacimiento"
                          label="Fecha de Nacimiento"
                          name="fecha"
                          v-model="fecha"
                          type="text"
                          color="secondary"
                        />
                      </v-form>
                     
                      <div class="text-center mt-3">
                        <v-btn
                          @click="enviar"
                          rounded
                          color="secondary"
                          elevation="13"
                          dark
                          >Consultar</v-btn
                        >
                      </div>
                    </v-card-text>
                  </v-col>
                </v-row>
              </v-window>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>
<script>

export default {
  components: {
  
  },
  layout: "login",
  data() {
    return {
      // alert: false,
      // usuario: "",
      // contra: "",
      // mensaje: "Usuario incorrecto",
      // tipoAlert: "error",
      // value: true,
    };
  },
  methods: {
    // async enviar() {
    //   try {
    //     const respuesta = await this.$axios.post(
    //       "api/sgcnegocio/iniciarSesion",
    //       {
    //         nombreUsuario: this.usuario,
    //         contrasena: this.contra,
    //       }
    //     );
    //     console.log(respuesta);
    //     if (!respuesta.data && !respuesta.data.nombre) {
    //       this.alert = true;
    //       this.usuario = "";
    //       this.contra = "";
    //     } else {
    //       this.$store.commit("session/logIn", respuesta.data);
    //       this.alert = false;
    //       let type = respuesta.data.usuario.role;

    //       if (type === "ADMIN") {
    //         this.$router.push("/user");
    //       } else if ((type = "REPRESENTANTE")) {
    //         this.$router.push("/userUniversidad");
    //       }
    //     }
    //   } catch (err) {
    //     console.log(err);
    //     console.log("entro");
    //     this.usuario = "";
    //     this.contra = "";
    //     this.$notifier.showMessage({
    //       content: "Corrija los campos del formulario para continuar",
    //       color: "success",
    //     });
    //   }
    // },
  },
};
</script>

<style>
.imagen {
  width: 100%;
}
.contenedor {
  padding: 30px;
}
.fondo {
  background: #36d1dc; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #486DBF,
    #c1c1e2
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #486DBF,
    #c1c1e2
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

</style>
