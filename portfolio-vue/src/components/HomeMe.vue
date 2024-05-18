<template>
    <div class="home">
      <h1>Bem-vindo ao meu portfólio</h1>
      <nav>
        <router-link to="/">Home</router-link> |
        <router-link to="/projects">Projetos</router-link> |
        <router-link to="/about">Sobre Mim</router-link> |
        <router-link to="/contact">Contato</router-link>
      </nav>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HomeMe'
  }
  </script>
  
  <style scoped>
  .home {
    text-align: center;
  }
  nav {
    margin-top: 20px;
  }
  </style>
  