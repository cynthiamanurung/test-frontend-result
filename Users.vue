<template>
  <div id="app">
    <Users />
  </div>
</template>

<script>
  import axios from 'axios';

  export default {
    name: 'Users',
    data() {
      return {
        users: null,
      };
    },
    created: function() {
      axios
        .get('https://jsonplaceholder.typicode.com/users')
        .then(res => {
          this.users = res.data;
        })
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>