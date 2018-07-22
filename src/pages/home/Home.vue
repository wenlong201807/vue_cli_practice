<template>
  <div>
    <h1 class="home">home，单文件组件</h1>
    <router-link to="/list" class="home">列表页</router-link>
  </div>

</template>

<script>
export default {
  name: 'Home'
}
</script>

<style scoped>
.home {
  font-size: 50px;
  color: red;
}
</style>
