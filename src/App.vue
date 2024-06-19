<script setup>
import { ref, computed } from 'vue';

const tempSi = ref(0);
const tempKelvin = computed(() => tempSi.value + 273.15);
const tempCelsius = computed(() => tempSi.value);
const volts = ref(0); // Ajout d'une nouvelle référence pour les volts
const watt = computed(() => volts.value * 2); // Calcul de la puissance en fonction des volts
</script>

<template>
  <input type="number" v-model="tempSi">
  <p>Kelvin: {{ tempKelvin }}</p>
  <p>Celsius: {{ tempCelsius }}</p>
  <input type="number" v-model="volts"> <!-- Ajout d'un nouvel input pour les volts -->
  <p>Watt: {{ watt }}</p> <!-- Affichage des watts -->
</template>

<style scoped></style>