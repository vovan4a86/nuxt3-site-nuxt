<template>
  <div class="container">
    <h1>Action</h1>
    <p v-if="$fetchState.pending">Fetching mountains...</p>
    <p v-else-if="$fetchState.error">An error occurred :(</p>
    <div v-else>
      <h1>Nuxt Mountains</h1>
      <ul>
        <li v-for="post of posts" :key="post.id">
          <NuxtLink :to="`/posts/${post.id}`" >{{ post.title }}</NuxtLink>
        </li>
      </ul>
      <button class="btn btn-info" @click="$fetch">Refresh</button>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      posts: []
    }
  },
  async fetch () {
    this.posts = await fetch(
      'https://api.nuxtjs.dev/posts'
    ).then(res => res.json())
  }
}
</script>

<style scoped>

</style>
