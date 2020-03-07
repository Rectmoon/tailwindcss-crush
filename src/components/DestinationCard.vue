<template>

  <div class="flex items-center rounded-lg bg-white shadow-lg overflow-hidden">
    <img
      :src="destination.img"
      alt=""
      class="w-32 h-32 flex-shrink-0"
    />
    <div class="px-6 py-4">
      <h3 class="sm:text-2xl font-semibold text-gray-800">{{destination.city}}</h3>
      <p class="text-gray-600">￥ {{destination.price}} / 晚</p>
      <div class="mt-4">
        <a
          href="#"
          class="text-indigo-500 hover:text-indigo-400 font-semibold"
        >Explore 76 properties</a>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  props: ['destination']
}
</script>
