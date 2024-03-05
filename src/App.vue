<script setup>
import BlogPost from "./components/BlogPost.vue";
import { ref } from "vue";

const posts = ref([
  { title: "Post 1", id: 1, body: "descripción 1" },
  { title: "Post 2", id: 2, body: "descripción 2" },
  { title: "Post 3", id: 3, body: "descripción 3" },
  { title: "Post 4", id: 4 },
])

const favorito = ref('')

const cambiarFavorito = (title) => {
  favorito.value = title;
}

</script>

<template>
  <div class="container">
    <h1>APP</h1>
    <h2>Mi Post Favorito: {{ favorito }}</h2>

    <BlogPost 
    v-for="post in posts"
    :key="post.id"
    :title="post.title" 
    :id="post.id" 
    :body="post.body"
    @cambiarFavorito="cambiarFavorito"
    ></BlogPost>

  </div>
</template>