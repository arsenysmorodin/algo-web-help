<template>
  <div
    :class="props.bgColor"
    class="text-black card w-96">
    <div class="card-body">
      <h2 class="font-bold card-title">{{ props.title }}</h2>
      <p class="font-semibold">{{ props.description }}</p>
      <div class="card-actions justify-end">
        <button class="btn btn-primary">Узнать больше</button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  title: { type: String, default: 'Title' },
  description: { type: String, default: 'Description' },
  bgColor: { type: String, default: 'bg-base-100' }
})
</script>
