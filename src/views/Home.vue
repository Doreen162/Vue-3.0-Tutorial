<template>
  <div class="home">
    home
    <p ref="p">My name is {{ name }} and my age is {{ 30 }}</p>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>
// Template refs
import { ref } from 'vue'

export default {
  name: 'Home',
  setup() {
    console.log('this')

    const p = ref(null)

    let name = 'mario'
    let age = 30

    const handleClick =() => {
      console.log(p, p.value)
      p.value.classList.add('test')
      p.value.textContent = 'hello, ninjas'
    }

    return { name, age, handleClick, p }

  },

//  created() {
//  console.log('created')
//  },
//  mounted() {
//    console.log('mounted')
//  }
}
</script>
