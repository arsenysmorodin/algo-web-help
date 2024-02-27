<template>
  <div>
    <div
      :style="style"
      class="text-white font-extrabold text-7xl max-w-screen-2xl mx-auto mb-24">
      <div class="max-w-5xl">
        <p class="mb-6"> Привет 👋 </p>
        <p class="mb-12">
          Занимаешься в Алгоритмике на курсах
          <span class="text-yellow-500">"Создание сайтов"</span>
          или&nbsp;<span class="text-purple-500">"Фронтенд"</span>
        </p>
        <p class="mb-6"> Тогда тебе точно понравится этот сайт!</p>
        <p> Здесь ты найдешь много крутых подсказок и полезных советов </p>
      </div>
    </div>
    <div class="max-w-screen-2xl mx-auto">
      <span class="text-5xl block font-extrabold mb-6">Например:</span>
      <div>
        <div class="flex flex-wrap gap-8 justify-between">
          <Card
            v-for="(_, i) in cardContent.length"
            :key="i"
            :title="cardContent[i].title"
            :description="cardContent[i].description"
            :bg-color="cardContent[i].bgColor" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import circle from '~/assets/decoration/circle.gif'

const style = {
  backgroundImage: `url(${circle})`,
  backgroundRepeat: 'no-repeat',
  backgroundPosition: 'center right -200px',
  backgroundSize: '1000px'
}

const cardContent = [
  {
    title: 'Все теги HTML',
    description:
      'Все HTML-теги собраны в одном месте и ждут когда ты их добавишь на свой сайт',
    bgColor: 'bg-red-500'
  },
  {
    title: 'Как сделать галерею',
    description: 'Инструкция, как сделать галерею-слайдер только на HTML и CSS',
    bgColor: 'bg-lime-500'
  },
  {
    title: 'Как сделать якорную ссылку',
    description: 'Что бы при нажатии страница перелистывалась к нужному блоку',
    bgColor: 'bg-cyan-500'
  },
  {
    title: 'Как стать крутым фронтенд-разработчиком',
    description: 'Что делать после курса "Фронтенд"?',
    bgColor: 'bg-violet-500'
  }
]
</script>
