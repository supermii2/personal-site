<template>
    <div class="home">
      <SearchBar/>
    </div>
</template>
  
<script lang="ts">
  import { defineComponent, onMounted, onBeforeUnmount } from 'vue';
  import SearchBar from '@/components/SearchBar.vue'; // @ is an alias to /src
  
  export default defineComponent({
    name: 'HomeView',
    components: {
      SearchBar,
    },
    setup() {
      onMounted(() => {
        document.body.style.backgroundImage = `url(${require('@/assets/background.jpg')})`;
        document.body.style.backgroundSize = 'cover';
        document.body.style.backgroundPosition = 'center';
        document.body.style.backgroundRepeat = 'no-repeat';
      });
  
      onBeforeUnmount(() => {
        // Reset body styles to default or to another background
        document.body.style.backgroundImage = '';
        document.body.style.backgroundSize = '';
        document.body.style.backgroundPosition = '';
        document.body.style.backgroundRepeat = '';
      });
    },
  });
</script>
  
<style scoped>
    .home {
      flex: 1;
      display: flex;
      justify-content: center;
      align-items: center;
    }
</style>
  