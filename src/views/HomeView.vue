<template>
  <div class="home">
    <HelloWorld msg="hi"/>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
<style scoped>
  .home{
    background-color: #f4f4f4;
  }
</style>
