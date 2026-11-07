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

const clickedFood = ref('')
const showFoodOnScreen = (foodName) => {
  clickedFood.value = foodName
}
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
   <button @click="showFoodOnScreen(user.favoriteFood)">
      Показати страву на екрані
    </button>
    <p v-if="clickedFood">Ви обрали: {{ clickedFood }}</p>
  </div>
</template>
