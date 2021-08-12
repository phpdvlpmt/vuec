<template>
<!--home content-->
<section>
  <h1 class="text-xl text-gray-900 px-4 font-bold">Vue Composition API - První seznámení</h1>
 <Plus></Plus>
 <Calc></Calc>
</section>
</template>

<script>

import Plus from '@/components/Plus.vue'
import Calc from '@/components/Calc.vue'

// @ is an alias to /src
//import Navigation from '@/components/Navigation.vue'

export default {
  name: 'Home',
  components: {
   Plus, Calc
    
    
  },
  setup() {
   
  }
}
</script>
