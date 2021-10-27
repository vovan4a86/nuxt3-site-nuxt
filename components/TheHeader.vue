<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container">
      <div class="collapse navbar-collapse" id="navbarsExample07">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item">
            <NuxtLink class="nav-link" to="/" exact-active-class="active" exact no-prefetch>Home</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="/allposts" exact-active-class="active" no-prefetch>Posts</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="/allbeers" exact-active-class="active" no-prefetch>Beers</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="/allplanets" exact-active-class="active" no-prefetch>Planets</NuxtLink>
          </li>
        </ul>
        <form class="form-inline my-2 my-md-0">
          <h1>Simple Header</h1>
        </form>
      </div>
    </div>
  </nav>
</template>

<style>
.nuxt-logo {
  height: 180px;
}
</style>
