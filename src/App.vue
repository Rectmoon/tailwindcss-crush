<template>
  <div class="app">
    <div class="bg-gray-100 flex">
      <div class="px-8 py-12 max-w-md mx-auto sm:max-w-xl lg:max-w-full lg:w-1/2 lg:py-24 lg:px-12">
        <div class="xl:max-w-lg xl:ml-auto">
          <img
            class="h-10"
            src="/images/1.png"
            alt="Workcation"
          >
          <img
            class="mt-6 rounded-lg shadow-xl sm:mt-8 sm:h-64 sm:w-full sm:object-cover sm:object-center lg:hidden"
            src="/images/2.png"
            alt="Woman workcationing on the beach"
          >
          <h1 class="mt-6 text-2xl font-bold text-gray-900 leading-tight sm:mt-8 sm:text-4xl lg:text-3xl xl:text-4xl">
            You can work from anywhere.
            <br class="hidden lg:inline"><span class="text-indigo-500">Take advantage of it.</span>
          </h1>
          <p class="mt-2 text-gray-600 sm:mt-4 sm:text-xl">
            Workcation helps you find work-friendly rentals in beautiful locations so you can enjoy some nice weather even when you're not on vacation.
          </p>
          <div class="mt-4 sm:mt-6">
            <a
              href="#"
              class="btn btn-indigo shadow-lg sm:text-base"
            >Book your escape</a>
          </div>
        </div>
      </div>
      <div class="hidden lg:block lg:w-1/2 lg:relative">
        <img
          class="absolute inset-0 h-full w-full object-cover object-center"
          src="/images/2.png"
          alt="Woman workcationing on the beach"
        >
      </div>
    </div>

    <div class="max-w-md sm:max-w-2xl lg:max-w-6xl mx-auto px-8 lg:px-12 py-8">
      <div class="flex flex-wrap -mx-4">
        <div
          v-for="(destination, index) in destinationData"
          :key="index"
          class='mt-6 w-full lg:w-1/2 xl:w-1/3'
        >
          <DestinationCard :destination="destination" />
        </div>
      </div>
    </div>

  </div>
</template>

<script>
import DestinationCard from '@/components/DestinationCard'

export default {
  components: { DestinationCard },

  data() {
    return {
      destinationData: [
        {
          city: '长沙',
          img: '/images/1.png',
          price: 100
        },
        {
          city: '库页岛',
          img: '/images/2.png',
          price: 200
        },
        {
          city: '贝加尔湖',
          img: '/images/3.png',
          price: 300
        },
        {
          city: '撒哈拉沙漠',
          img: '/images/4.png',
          price: 400
        },
        {
          city: '帕米尔高原',
          img: '/images/5.png',
          price: 500
        },
        {
          city: '青海湖',
          img: '/images/6.png',
          price: 600
        }
      ]
    }
  }
}
</script> 

