<template>
<div id="app">
  {{ user.username }} - {{fullName}}
  <strong>
    
  </strong>
</div>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      followers: 0,
      user: {
        id:1,
        username: '@_adamKogan',
        firstName: 'Adam',
        lastName: 'Kogan',
        email: 'adam.kogan7@gmail.com',
        isAdmin:true
      }
    }
  },
  computed: {
    fullName() {
      return `${this.user.firstName} ${this.user.lastName}`;
    }
  },
  methods: {
    followUser() {
      this.followers++
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
