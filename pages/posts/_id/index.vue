<template>
  <div>
    <h1>hello</h1>
<!--    <h1>{{ post.description }}</h1>-->
  </div>
</template>

<script>
export default {
  data () {
    return {
      mountains: []
    }
  },
  asyncData (ctx) {
    const mountains = fetch(
      'https://api.nuxtjs.dev/mountains'
    ).then(res => res.json())
    const mount = mountains.find(mount => mount.slug === ctx.params.slug)
    console.log(mount)
  }

}
</script>
