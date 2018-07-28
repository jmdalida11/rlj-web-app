<template>
  <v-container>
    <v-flex xs12 sm6 offset-sm3>
    <h2>Registration</h2>
    <v-form ref="form" v-model="valid" lazy-validation>
      <v-text-field
        v-model="firstname"
        label="Firstname"
        required
      ></v-text-field>
      <v-text-field
        v-model="lastname"
        label="Lastname"
        required
      ></v-text-field>
      <v-text-field
        v-model="middlename"
        label="Middlename"
        required
      ></v-text-field>
      <v-text-field
        v-model="username"
        label="Username"
        required
      ></v-text-field>
      <v-text-field
        v-model="password"
        :type="'password'"
        label="Password"
        required
      ></v-text-field>
      <v-text-field
        v-model="bday"
        label="Birthday"

        required
      ></v-text-field>
      <v-text-field
        v-model="email"
        label="E-mail"
        required
      ></v-text-field>
      <v-text-field
        v-model="contact"
        label="Contact"
        required
      ></v-text-field>
      <v-text-field
        v-model="address"
        label="Address"
        required
      ></v-text-field>
      <v-btn
        :disabled="!valid"
        @click="submit"
      >
        Register
      </v-btn>
      <v-btn @click="clear">clear</v-btn>
    </v-form>
    </v-flex>
  </v-container>
</template>

<script>
export default {
  name: 'Registration',
  data () {
    return {
      firstname: '',
      lastname: '',
      middlename: '',
      username: '',
      password: '',
      bday: '',
      email: '',
      contact: '',
      address: '',
      valid: false
    }
  },
  methods: {
    submit () {

    },
    clear () {
    }
  }
}
</script>

<style scoped>

</style>
