<script setup>
import { ref, computed } from 'vue'

const intereses = ref([
  'Me interesan los proyectos que combinan calidad de software, análisis de datos y mejora continua, especialmente en entornos donde se promueva el aprendizaje constante y la colaboración entre equipos técnicos.',
  'Busco seguir desarrollándome en áreas como QA Manual, Automatización de Pruebas, Data Analytics y Python, aplicando metodologías ágiles y herramientas que optimicen los procesos de desarrollo.',
  'También me motiva participar en equipos donde la innovación y la comunicación efectiva sean pilares para alcanzar resultados de calidad.'
])

// Un solo texto
const interesesTexto = computed(() => intereses.value.join(' '))
</script>

<template>
  <div class="intereses-contenedor">
    <FondoLava />
    <p class="intereses-texto">
      {{ interesesTexto }}
    </p>
  </div>
</template>

<style scoped>
.intereses-contenedor {
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
}
.intereses-texto {
  font-size: 1.6rem;       /*  cambia a gusto: 1.8rem, 2rem, etc. */
  line-height: 1.8;        /* más aire entre líneas */
  color: var(--vt-c-white-soft); /* color claro */
  text-align: center;      /* centrado */
  max-width: 80ch;         /* ancho óptimo para lectura */
  margin: 0 auto;          /* centrado horizontal */
  text-shadow: 1px 1px 4px rgba(0,0,0,.8); /* mejora contraste */
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.4rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
}

.item {
    margin-bottom: 1rem;
}
</style>