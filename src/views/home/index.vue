<!--
    文件：src/views/home/index.vue
    作者：Pi
    时间：2019/07/22
    描述：首页
-->

<template>
  <section class="home-page">
    <p>{{ name }}</p>
    <p>{{ desc }}</p>
    <router-link to="/test">内嵌路由</router-link>
    <router-view></router-view>
  </section>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  computed: {
    ...mapGetters({
      name: 'User/getName',
      desc: 'User/getDesc'
    })
  }
}
</script>

<style lang="less" scoped>
</style>