<script>
import AuthenticationService from '@/services/AuthenticationService'
export default {
    data () {
        return {
            email: '',
            password: ''
        }
    },

    methods: {
        async register () {
            const response = await AuthenticationService.register({
                email: this.email,
                password: this.password
            })

            console.log(response.data);
        }
    }   
};
</script>

<template>
  <div class="greetings">
      <h1>Register</h1>
      <input type="email" placeholder="email" name="email" v-model="email" />
      <br>
      <input type="password" placeholder="password" name="password" v-model="password"/>
      <br>
      <button @click="register">Register</button>
  </div>
</template>


<style scoped>
</style>
