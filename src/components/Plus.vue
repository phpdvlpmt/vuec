<template>
  <div class="px-4 py-2 mt-2 space-y-1 border-b-2 border-gray-200">
    <h2 class="text-lg text-gray-700 font-semibold">Components Plus<span class="ml-2 text-gray-300 text-sm">proměnné a funkce (let num = ref(0), 
        const handleclick = () => {} return {}</span></h2>
    <button class="block px-3 py-2 bg-green-600 hover:bg-green-900 text-white rounded-lg transition delay-300" @click="handleClick()">Klikni pro zvýšení</button>
    <p>Kliknul jsi {{ numOfClicks }} krát.</p>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'
// @ is an alias to /src
//import Navigation from '@/components/Navigation.vue'

export default {
  name: 'Plus',
  components: {
   
  },
  setup() {
    let numOfClicks = ref(0)
    const handleClick = () => {
      numOfClicks.value++
    }
    return {
      numOfClicks, handleClick
    }
  }
}
</script>

<style>

</style>