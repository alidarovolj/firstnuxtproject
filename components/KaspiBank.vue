<template>
  <div class="my-5 container mx-auto">
    <h2 class="text-5xl font-bold text-center mb-4">
      Интернет-магазин на Kaspi.kz
    </h2>
    <div class="flex flex-wrap justify-content items-center">
      <div v-for="item of mainPage" :key="item.id" class="w-1/5 p-2">
        <p class="text-center text-lg">
          {{ item.name }}
        </p>
        <img class="w-full" :src="item.image" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'KaspiBank',
  data () {
    return {
      mainPage: [
        {
          id: 1,
          name: 'Телефоны и гаджеты',
          test: [
            {
              name: 'hello'
            }
          ],
          image: 'https://kaspi.kz/yml/main-navigation/n/n//image/desktop-categories-Smartphones%20and%20gadgets'
        },
        {
          id: 2,
          name: 'Компьютеры',
          image: 'https://kaspi.kz/img/apple-2x.png'
        },
        {
          id: 3,
          name: 'Тв, Аудио, Видио',
          image: 'https://kaspi.kz/img/shoes-2x.png'
        },
        {
          id: 4,
          name: 'Бытовая техника',
          image: 'https://kaspi.kz/img/clothes-2x.png'
        },
        {
          id: 5,
          name: 'Автотовары',
          image: 'https://kaspi.kz/img/decorations-2x.png'
        },
        {
          id: 6,
          name: 'Детские товары',
          image: 'https://kaspi.kz/img/sport-2x.png'
        },
        {
          id: 7,
          name: 'Товары для дома',
          image: 'https://kaspi.kz/img/beauty-2x.png'
        },
        {
          id: 8,
          name: 'Красота и здоровье',
          image: 'https://kaspi.kz/img/pets-2x.png'
        },
        {
          id: 9,
          name: 'Обувь',
          image: 'https://kaspi.kz/img/gifts-2x.png'
        },
        {
          id: 10,
          name: 'Одежда',
          image: 'https://kaspi.kz/img/media-2x.png'
        }
      ]
    }
  }
}
</script>
