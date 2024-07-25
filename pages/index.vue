<template>
    <div>
      <h1>Daftar Artikel</h1>
      <div v-if="loading">Loading...</div>
        <ul>
          <li v-for="article in articles" :key="article.id">
            <h2>{{ article.title }}</h2>
            <p>{{ article.body }}</p>
          </li>
        </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        articles: [],
        loading: true
      };
    },
    async created() {
      try {
        const response = await fetch('https://jsonplaceholder.typicode.com/posts');
        this.articles = await response.json();
      } catch (error) {
        console.error('Error fetching articles:', error);
      } finally {
        this.loading = false;
      }
    }
  };
  </script>
  
  <style scoped>
  h1 {
    text-align: center;
    margin-bottom: 20px;
  }
  h2 {
    margin: 10px 0 5px;
  }
  p {
    margin: 0 0 20px;
  }
  </style>
  