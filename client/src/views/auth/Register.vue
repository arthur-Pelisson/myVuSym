<template>
  <div class="ls">
    <b-card-group deck>
      <b-container id="container-form">
        <b-row class="justify-content-md-center">
          <b-col>
            <b-card
              
              header-text-variant="white"
              header-tag="header"
              header-bg-variant="dark"
              class="sm"
              footer-tag="footer"
              footer-bg-variant="dark"
            >
              <template #header>
                <h6 class="mb-0">Crée un compte</h6>
              </template>
              <div>
                <b-form @submit="onSubmit" @reset="onReset" v-if="show">
                  <b-form-group
                    id="input-group-1"
                    label="Login"
                    label-for="input-1"
                  >
                    <b-form-input
                      id="input-1"
                      v-model="form.login"
                      placeholder="Entre votre login"
                      required
                    ></b-form-input>
                  </b-form-group>

                  <b-form-group
                    id="input-group-2"
                    label="Adresse email:"
                    label-for="input-2"
                    description="Nous ne partageron j'amais votre address email"
                  >
                    <b-form-input
                      id="input-2"
                      v-model="form.email"
                      type="email"
                      placeholder="Entré votre addrese email"
                      required
                    ></b-form-input>
                  </b-form-group>

                  <b-form-group
                    id="input-group-3"
                    label="Mot de passe"
                    label-for="input-3"
                  >
                    <b-form-input
                      id="input-3"
                      v-model="form.password"
                      placeholder="Entre votre mot de passe"
                      type="password"
                      required
                    ></b-form-input>
                  </b-form-group>

                  <b-form-group
                    id="input-group-4"
                    label="Confirm mot de passe"
                    label-for="input-4"
                  >
                    <b-form-input
                      id="input-4"
                      v-model="form.confirmPassword"
                      placeholder="Confirmer votre mot de passe"
                      type="password"
                      required
                    ></b-form-input>
                  </b-form-group>

                  <b-form-group
                    id="input-group-5"
                    label="Sexe"
                    label-for="input-5"
                  >
                    <b-form-select
                      id="input-5"
                      v-model="form.sex"
                      :options="sexs"
                      required
                    ></b-form-select>
                  </b-form-group>
                  <b-button type="submit" variant="primary">Register</b-button>
                </b-form>
              </div>
              <template #footer>
                <em></em>
              </template>
            </b-card>
          </b-col>
        </b-row>
      </b-container>
    </b-card-group>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        login: '',
        email: '',
        password: '',
        confirmPassword: '',
        sex: null,
      },
      sexs: [
        { text: 'Selectioner votre sex', value: null },
        'Femme',
        'Homme',
        'Non binaire',
      ],
      show: true,
    };
  },
  methods: {
    onSubmit(event) {
      event.preventDefault();
      alert(JSON.stringify(this.form));
    },
  },
};
</script>

<style>
#container-form {
  width: 50em;
  margin-top: 10em;
}
</style>