<template>
  <div class="home">
  <h1>home</h1>
  <h2>refs</h2>
  <p>{{ninjaOne.name}} - {{ninjaOne.age}}</p>
  <button @click="updateNinjaOne">update ninja one</button>
  <h2>reactive</h2>
  <p>{{ninjaTwo.name}} - {{ninjaTwo.age}}</p>
  <button @click="updateNinjaTwo">update ninja two</button>
  </div>
</template>

<script>
import { reactive, ref } from 'vue'

export default {
  name: 'Home',
  setup() {
    const ninjaOne = ref({name: 'kevin', age: 30})
    const ninjaTwo = reactive({name: 'bob', age: 40})

    const updateNinjaOne = () => {
      ninjaOne.value.age = 40
    }
    const updateNinjaTwo = () => {
      ninjaTwo.age = 45
    }

    return {ninjaOne, updateNinjaOne, ninjaTwo, updateNinjaTwo}
  }
}
</script>
