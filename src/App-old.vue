<template>
  <!-- <router-link to="/">首頁</router-link>
  <router-link to="/guitar">吉他</router-link> -->
  <input type="button" value="首頁" @click="goto('/')">
  <input type="button" value="吉他" @click="goto('/guitar')">
  <input type="button" value="顯示路由" @click="showInfo">
  <router-view />
</template>
{{$router }}
<script setup>
import { useRouter, useRoute } from 'vue-router'
const route = useRoute()
const router = useRouter()
const goto = (path) => {
  router.push(path)
}
const showInfo = () => {
  console.log(route.fullPath)
}
</script>
