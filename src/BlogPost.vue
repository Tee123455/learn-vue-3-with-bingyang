<template>
  <div class="blog-post">
    <p>
      {{ message }}
    </p>
    <h2>{{ id }} - {{ blogPostTitle }}</h2>
    <h4>{{ blogPostContent }}</h4>
    <button @click="blogPostTitle= 'A different title'">Change Blog Post Title</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

let message = ref('This is the BlogPost component.')
const props = defineProps(['id', 'blogPostTitle', 'blogPostContent'])
</script>

<style scoped>
.blog-post {
  background-color: aqua;
  padding: 10px;
  margin-bottom: 10px;
}
</style>