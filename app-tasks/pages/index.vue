<template>
  <div class="login-container">
    <center>
      <h1>Bienvenidos a la app de tareas</h1>
      <p>Esta es una aplicación que permite gestionar las tareas de los estudiantes</p>

      <a href="/tareas">Click para iniciar (sin nuxtLink)</a>
<br>
<br>
      <NuxtLink to="/tareas">
        Click para iniciar (Con nuxtLink)
      </NuxtLink>


      <h2 class="login-title">Iniciar Sesión</h2>
    <form @submit.prevent="login" class="login-form">
      <div class="form-group">
        <label for="email">Correo Electrónico:</label>
        <input type="email" id="email" v-model="email" required class="form-control">
      </div>
      <div class="form-group">
        <label for="password">Contraseña:</label>
        <input type="password" id="password" v-model="password" required class="form-control">
      </div>
      <button type="submit" class="login-button">Iniciar Sesión</button>
    </form>

    </center>

  </div>
</template>
<script>
definePageMeta({
  layout: "blank",
});


</script>

<style scoped>
.login-container {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.login-title {
  text-align: center;
}

.login-form {
  display: flex;
  flex-direction: column;
}

.form-group {
  margin-bottom: 10px;
}

label {
  font-weight: bold;
}

.form-control {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 3px;
  font-size: 16px;
}

.login-button {
  background-color: #007BFF;
  color: #fff;
  padding: 10px;
  border: none;
  border-radius: 3px;
  font-size: 16px;
  cursor: pointer;
}

.login-button:hover {
  background-color: #0056b3;
}
</style>