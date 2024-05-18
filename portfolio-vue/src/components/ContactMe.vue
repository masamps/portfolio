<template>
    <div class="contact-me">
      <h1>Contato</h1>
      <form>
        <label for="name">Nome:</label>
        <input type="text" id="name" name="name">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email">
        <label for="message">Mensagem:</label>
        <textarea id="message" name="message"></textarea>
        <button type="submit">Enviar</button>
      </form>
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .contact-me {
    text-align: center;
  }
  form {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  label {
    margin-top: 10px;
  }
  input, textarea {
    width: 100%;
    max-width: 400px;
    margin-top: 5px;
  }
  button {
    margin-top: 20px;
  }
  </style>
  