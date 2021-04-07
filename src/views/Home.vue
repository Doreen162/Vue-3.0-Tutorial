<template>
  <div class="home">
    home
    <p>My name is {{ name }} and my age is {{ 30 }}</p>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>
export default {
  name: 'Home',
  setup() {
    console.log('setup')

    let name = "mario"
    let age = 30

    const handleClick =() => {
      console.log('you clicked me')
    }

    return { name, age, handleClick }

  },

//  created() {
//  console.log('created')
//  },
//  mounted() {
//    console.log('mounted')
//  }
}
</script>
