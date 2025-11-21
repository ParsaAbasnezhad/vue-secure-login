<template>
  <div class="container">
    <HeaderSite @login="showLogin" @register="showRegister" />

    <LoginForm v-if="currentPage === 'login'" />
    <RegisterForm v-if="currentPage === 'register'" />
  </div>
</template>

<script>
import HeaderSite from './components/HeaderSite.vue';
import LoginForm from './components/LoginForm.vue';
import RegisterForm from './components/RegisterForm.vue';

export default {
  name: 'App',
  components: {
    HeaderSite,
    LoginForm,
    RegisterForm
  },
  data() {
    return {
      currentPage: 'login'
    }
  },
  methods: {
    showLogin() {
      this.currentPage = 'login'
    },
    showRegister() {
      this.currentPage = 'register'
    }
  }
}
</script>

<style>
.container {
  width: 1300px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  margin: 0 auto;
}
</style>
