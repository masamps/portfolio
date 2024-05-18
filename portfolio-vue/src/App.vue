<script setup>
import { ref } from 'vue'
// import emailjs from 'emailjs-com'

const form = ref({
  name: '',
  email: '',
  message: ''
})

const successMessage = ref('')

const sendEmail = () => {
  // emailjs.send(
  //   'YOUR_SERVICE_ID',
  //   'YOUR_TEMPLATE_ID',
  //   form.value,
  //   'YOUR_USER_ID'
  // ).then(response => {
  //   successMessage.value = 'Mensagem enviada com sucesso!'
  // }).catch(error => {
  //   successMessage.value = 'Ocorreu um erro ao enviar a mensagem.'
  // })
}
</script>

<template>
  <div id="app">
    <header>
      <h1>Meu Portfólio</h1>
      <nav>
        <a href="#home">Home</a>
        <a href="#projects">Projetos</a>
        <a href="#about">Sobre Mim</a>
        <a href="#contact">Contato</a>
      </nav>
    </header>
    <main>
      <section id="home" class="section">
        <h2>Bem-vindo ao meu portfólio</h2>
      </section>
      <section id="projects" class="section">
        <h2>Projetos</h2>
        <!-- Adicione aqui seus projetos -->
      </section>
      <section id="about" class="section">
        <h2>Sobre Mim</h2>
        <p>Sou um desenvolvedor Full Stack com experiência em...</p>
      </section>
      <section id="contact" class="section">
        <h2>Contato</h2>
        <form @submit.prevent="sendEmail">
          <div class="form-group">
            <label for="name">Nome:</label>
            <input type="text" id="name" v-model="form.name" required>
          </div>
          <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" id="email" v-model="form.email" required>
          </div>
          <div class="form-group">
            <label for="message">Mensagem:</label>
            <textarea id="message" v-model="form.message" required></textarea>
          </div>
          <button type="submit" class="btn">Enviar</button>
        </form>
        <p v-if="successMessage">{{ successMessage }}</p>
      </section>
    </main>
    <footer>
      <p>&copy; 2024 Meu Nome. Todos os direitos reservados.</p>
    </footer>
  </div>
</template>

<style scoped>
#app {
  text-align: center;
  font-family: 'Arial', sans-serif;
  background-color: #f4f4f9;
  color: #333;
}

header {
  background-color: #333;
  color: white;
  padding: 20px 0;
}

nav {
  margin-top: 10px;
}

nav a {
  margin: 0 15px;
  color: white;
  text-decoration: none;
  font-weight: bold;
}

nav a:hover {
  text-decoration: underline;
}

main {
  padding: 20px;
}

.section {
  padding: 50px 20px;
  margin: 20px 0;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 20px;
  text-align: left;
}

.form-group label {
  display: block;
  font-weight: bold;
  margin-bottom: 5px;
}

.form-group input, .form-group textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.form-group textarea {
  resize: vertical;
}

.btn {
  display: inline-block;
  padding: 10px 20px;
  color: white;
  background-color: #333;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-weight: bold;
}

.btn:hover {
  background-color: #555;
}

footer {
  margin-top: 20px;
  padding: 10px 0;
  background-color: #333;
  color: white;
}
</style>
