<template>
  <div>
    <div class="text-xl mb-2">{{ count }}</div>
    <div>
      <button class="border border-indigo-500 text-indigo-500 rounded-md px-4 py-2 transition duration-500 ease select-none hover:text-white hover:bg-indigo-600 focus:outline-none focus:shadow-outline" @click="countUp">count up</button>
    </div>
    <div>
      <button class="mt-2 border border-indigo-500 text-indigo-500 rounded-md px-4 py-2 transition duration-500 ease select-none hover:text-white hover:bg-indigo-600 focus:outline-none focus:shadow-outline" @click="clear">clear</button>
    </div>
    <div v-if="count % 2 !== 0">odd</div>
  </div>
</template>

<script setup lang='ts'>
import { ref } from 'vue';

const title = ref("My Vitesse App");
const count = ref(0)

const countUp = () => {
  count.value++;
}

const clear = () => {
  count.value = 0;
}

</script>
