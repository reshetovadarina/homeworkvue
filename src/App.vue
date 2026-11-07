<script setup>
import { ref } from 'vue'

const user = ref({
  name: 'Дарина',
  city: 'Хмельницький',
  favoriteFood: 'Лазання'
})
</script>

<template>
  <div>
    <h2>Інформація про мене</h2>
    <p>Ім'я: {{ user.name }}</p>
    <p>Місто: {{ user.city }}</p>
    <p>Улюблена страва: {{ user.favoriteFood }}</p>
  </div>
</template>
