<template>
  <Navbar/>
  <router-view/>
  <Cards/>
  <FooterView/>
</template>
<script>
import FooterView from '@/components/Footer'
import Navbar from '@/components/Navbar'
import Cards from '@/components/cards.vue'
export default {
  components: {
    FooterView,
    Navbar,
    Cards
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
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>