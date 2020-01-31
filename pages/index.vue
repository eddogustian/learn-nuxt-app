<template>
  <div class="container">
    <h1>Home page 🚀</h1>
    <NuxtLink to="/about">
      About page
    </NuxtLink>
    <NuxtLink to="/profile">
      Profile page
    </NuxtLink>
    <hr>
    <h1>User Agent</h1>
    <p>{{ userAgent }}</p>
    <p>
      <NuxtLink to="/posts">
        Blog
      </NuxtLink>
    </p>
  </div>
</template>
<script>
export default {
  asyncData: ({ req }) => ({
    userAgent: (req ? req.headers['user-agent'] : (typeof navigator !== 'undefined' ? navigator.userAgent : 'No user agent (generated)'))
  }),
  head: {
    title: 'Home page 🚀',
    meta: [
      { hid: 'description', name: 'description', content: 'Home page description' }
    ],
    noscript: [
      { innerHTML: 'Body No Scripts', body: true }
    ],
    script: [
      { src: '/head.js' },
      // Supported since 1.0
      { src: '/body.js', body: true },
      { src: '/defer.js', defer: '' }
    ]
  }
}
</script>

<style>
.container {
  text-align: center;
  margin-top: 150px;
  font-size: 20px;
}
</style>
