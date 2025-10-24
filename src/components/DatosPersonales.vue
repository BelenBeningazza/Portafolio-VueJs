<script setup>
import linkedin from '/src/assets/linkedin_icon.svg';
import github from '/src/assets/github_icon.svg';

const title = 'Beningazza Luciana Belén';
const descripcion = 'Técnica Universitaria en Programación - UTN';
const residencia = 'Junín, Mendoza, Argentina';
const presentacion = 'Hola, Bienvenidos a mi potfolio de proyectos. Soy una desarrolladora web y mobile, me especializo ademas en QA manual y Automation, y también en Analisis de Datos. Apacionada de Java y Python.';
const redesSociales = [
  { id: 1, name: 'linkedin', src: linkedin, url: 'https://www.linkedin.com/in/luciana-belen-beningazza/' },
  { id: 2, name: 'github', src: github, url: 'https://github.com/belenBeningazza' },
  ];
const telefono = '+54 2634677512';
</script>

<template>
<section class="Datos personales">
    <div class = "card">
        <h1>{{ title }}</h1>
        <h2>{{ descripcion }}</h2>
        <p>{{ presentacion }} </p>
        <ul class="Conteiner-lista">
            <li v-for="red in redesSociales" :key = "red.id">
                <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
            </li>
        </ul>
        <h3>☎ Mi teléfono personal: {{ telefono }} </h3>
        <h4>{{ residencia }}</h4>

    </div>

</section>
</template>

<style scoped>
h1 {
  font-size: 2.5rem;
}

p {
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 1rem;
}

.card {
  background-color: rgb(28, 41, 52);
  border-radius: 10px;
  padding: 10px;
  margin: 10px;
  text-align: center;
}

.container-lista {
  display: flex;
  justify-content: center;
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: center;
}

.icon-redsocial {
  align-items: center;
  background-color: aliceblue;
  border-radius: 50%;
  padding: 2px;
  margin: 5px;
  box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}

.icon-redsocial:hover {
  background-color: rgb(28, 41, 52);
  box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

h3 {
  font-size: 1.2rem;
  font-weight: 600;
}
</style>