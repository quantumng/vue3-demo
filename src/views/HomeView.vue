<script setup>
import {
  // RouterLink,
  RouterView,
} from "vue-router";
import { ref, reactive } from "vue";
const msg = ref("hello world!");
const user = reactive({
  name: "John",
  age: 30,
});
</script>

<template>
  <el-container>
    <el-header>Header</el-header>
    <el-container>
      <el-aside width="200px">Aside</el-aside>
      <el-main><RouterView /></el-main>
    </el-container>
  </el-container>
</template>

<style lang="scss">
.btn {
  width: 200px;
  height: 50px;
}
</style>
