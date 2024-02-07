<template>
  <div>
    <ul>
      <li v-for="post in posts" :key="post.title">
        <p>{{ post.title }}</p>
      </li>
    </ul>
  </div>
</template>

<script lang="ts" setup>

// fetch blogs with nuxt/content plugin
const { data: posts } = await useAsyncData('blog', () => queryContent('/blog').find())


</script>
