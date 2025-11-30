<template>
  <ul class="news-list">
    <li>编号：{{ id }}</li>
    <li>标题：{{ title }}</li>
    <li>内容：{{ content }}</li>
  </ul>
</template>

<script setup lang="ts" name="About">
import { toRefs, computed } from 'vue'
import { useRoute } from 'vue-router'
let route = useRoute()
//let { query } = toRefs(route)
//console.log(query);
const id = computed(() => route.query.id)
const title = computed(() => route.query.title)
const content = computed(() => route.query.content)


</script>

<style scoped>
.news-list {
  list-style: none;
  padding-left: 20px;
}

.news-list>li {
  line-height: 30px;
}
</style>