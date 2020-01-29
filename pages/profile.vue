<template>
  <div>
    <h2>Hello Dude!</h2>
    <p>{{ message }}</p>
    <input v-model="message" type="text">
    <button @click="showAlert">
      Show Message
    </button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      message: 'Nuxt it\'s so cool..'
    }
  },
  methods: {
    showAlert (e) {
      alert(this.message)
    }
  }
}
</script>
