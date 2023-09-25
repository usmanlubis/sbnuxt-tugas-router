<template>
  <main class="container">
    <div v-for="article in articles" :key="article.title">
      <article v-if="article.title == paramTitle">
        <h2 class="text-center">{{article.title}}</h2>
        <img :src="article.img" :alt="article.img">
        <p>{{ article.content }}</p>
      </article>
    </div>
    <button class="btn btn-primary mb-4 m-auto d-block" @click="$router.go(-1)">Kembali</button>
  </main>
</template>

<script>
  export default {
    data() {
      return {
        paramTitle: this.$route.params.title,
        articles: [
        {
          title: 'Judul Artikel 1',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat dolor explicabo sint quos exercitationem fugiat reiciendis assumenda. Ad quia veritatis, dolor odit, voluptas numquam modi porro eius reprehenderit ullam tenetur?',
          img: 'https://images.unsplash.com/photo-1649282806617-c51bb282899c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80',
        },
        {
          title: 'Judul Artikel 2',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat dolor explicabo sint quos exercitationem fugiat reiciendis assumenda. Ad quia veritatis, dolor odit, voluptas numquam modi porro eius reprehenderit ullam tenetur?',
          img: 'https://images.unsplash.com/photo-1635732646038-0a1a2fe3f2d6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80',
        },
        {
          title: 'Judul Artikel 3',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat dolor explicabo sint quos exercitationem fugiat reiciendis assumenda. Ad quia veritatis, dolor odit, voluptas numquam modi porro eius reprehenderit ullam tenetur?',
          img: 'https://images.unsplash.com/photo-1640006807976-a6127e9d6fa0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80',
        },
      ],
      }
    },
  }
</script>

<style>
  h2 {
    margin-bottom: 20px;
  }

  img {
    display: block;
    width: 90%;
    max-width: 720px;
    margin: auto;
  }

  p {
    margin-top: 15px
  }
</style>