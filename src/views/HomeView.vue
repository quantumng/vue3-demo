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
    <el-header>
      <div class="logo">Quantum</div>
      <div class="menu">
        <el-dropdown split-button type="primary" @click="handleClick">
          个人中心
          <template #dropdown>
            <el-dropdown-menu>
              <el-dropdown-item>退出</el-dropdown-item>
            </el-dropdown-menu>
          </template>
        </el-dropdown>
      </div>
    </el-header>
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
