<template>
  <div class="container">
    <div>
      <div>
        <p>Hi from {{ name }}</p>
        <h2>Ini Halaman About</h2>
        <NLink to="/">
          Home page
        </NLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  asyncData () {
    return {
      name: process.static ? 'static' : (process.server ? 'server' : 'client')
    }
  },
  head: {
    title: 'About page'
  }
}
</script>
