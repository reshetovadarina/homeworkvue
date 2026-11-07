<script setup>
import { ref } from 'vue'

const user = ref({
  name: 'Дарина',
  city: 'Хмельницький',
  favoriteFood: 'Лазання',
    avatarUrl: 'https://gumoreska.in.ua/wp-content/uploads/2023/11/privit-kartinki-i-listivki-3.jpg',
  avatarAlt: 'Фото',
  isSpicy: false
})
</script>

<template>
  <div>
    <h2>Інформація про мене</h2>
    <img :src="user.avatarUrl" :alt="user.avatarAlt" />
    <p>Ім'я: {{ user.name }}</p>
    <p>Місто: {{ user.city }}</p>
    <div :class="{ 'is-hot': user.isSpicy }">
    <p>Улюблена страва: {{ user.favoriteFood }}</p>
  </div>
  </div>
</template>
