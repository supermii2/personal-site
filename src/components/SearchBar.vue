<template>
    <div class="search-bar">
      <input
        type="text"
        v-model="searchQuery"
        @keydown.enter="redirectToPage"
      />
    </div>
  </template>
  
<script>
  export default {
    data() {
      return {
        searchQuery: ''
      };
    },
    methods: {
      redirectToPage() {
        this.$router.push(this.searchQuery);
      }
    }
  };
</script>
  
<style scoped>
  .search-bar {
    margin: 20px;
    flex: 1;
    padding-bottom: 100px;
    padding-right: 15px;
  }
  input {
    padding: 10px;
    width: 300px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
</style>