<template>
  <div class="container d-flex flex-column justify-content-center align-items-center gap-3">
    <h2>Klik tombol di bawah untuk melihat artikel</h2>
    <NuxtLink to="/articles" class="btn btn-primary">Lihat artikel</NuxtLink>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  layout: 'home',
}
</script>
