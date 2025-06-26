<template>
  <div id="app">
    <Navbar :logo="logo_src" :alt="app_name" />
    <main>
      <router-view />
    </main>
    <FooterBox />
  </div>
</template>

<script>
  import Navbar from './components/Navbar.vue'
  import FooterBox from './components/Footer.vue'
  import LogoImage from '@/assets/img/logo.png'

  export default{
    name: "App",
    components: {
      Navbar,
      FooterBox
    },
    data(){
      return{
        logo_src: LogoImage,
        app_name: "Make Your Burger"
      }
    }
  }

</script>

<style>

  #app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  main {
    flex: 1;
  }

  *{
    font-family: Helvetica;
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  .main-container{
    margin: 50px;
    min-height: 250px;
  }

  h1{
    text-align: center;
    font-size: 42px;
    margin-bottom: 30px;
    color: #222;
  }
</style>
