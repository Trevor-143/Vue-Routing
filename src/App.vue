<template>

  <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{ name: 'AboutView'}">About</router-link> |
    <router-link :to="{ name: 'Jobs'}">jobs</router-link> 
  </nav>
  <button @click="redirect">Redirect</button>
  <button @click="back">Go back</button>
  <button @click="forward">Go forward</button>

  <router-view/>

</template>

<script>
  export default {
    methods: {
      redirect() {
        this.$router.push({name: 'HomeView'})
      },
      back() {
        this.$router.go(-1)
      },
      forward() {
        this.$router.go(+1)
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
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
} 

nav a.router-link-exact-active {
  background: #277351;
  color: #ffffff;
  padding: 10px 20px;
  border-radius: 5px;
}
button {
  margin: 10px;
  padding: 8px 16px;
  border: none;
  background: rgb(220, 220, 220);
  border-radius: 6px;
  font-family: inherit;
  transition: 0.4s;
  cursor: pointer;
}
button:hover {
  background: #277351;
  color: #ffffff;
}
</style>
