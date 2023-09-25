<template>
  <div id="app">
    <HeaderComponent />
    <Nuxt />
  </div>
</template>

<script>
  import HeaderComponent from '@/components/HeaderComponent';

  export default {
    components: {
      HeaderComponent
    }
  }
</script>
