<template>
  <div class="px-4 py-2 mt-2 space-y-1 border-b-2 border-gray-200">
      <h2 class="text-lg text-gray-700 font-semibold">Components Calc<span class="ml-2 text-gray-300 text-sm">proměnné a funkce (let num = ref(0), 
        const addNumbers = () => {} return {}</span></h2>
      <form class=" space-x-2">
            <input type="text" class="border-2 border-gray-300 px-2 py-1" v-model="num1">
            <input type="text" class="border-2 border-gray-300 px-2 py-1" v-model="num2">
            <button @click="addNumbers" type="button" class=" bg-red-500 hover:bg-red-600 text-white transition delay-300 py-2 px-4 rounded-lg">
            Add me!
        </button>
        </form>
        <p><strong>Sum:</strong> {{ sum }}</p>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
name: "Calc",

setup() {
 let num1 = ref(0)
 let num2 = ref(0)
 let sum = ref(0)
 
 const addNumbers = () => {
     sum.value = parseInt(num1.value) + parseInt(num2.value)
 }
 return {
     num1, num2, sum, addNumbers
 }
}
}
</script>

<style>

</style>