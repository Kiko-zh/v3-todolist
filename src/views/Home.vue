<template>
  <div class="container">
    <nav class="navbar navbar-expand-lg navbar-light bg-light mb-3">
      <a class="navbar-brand d-flex align-items-center" href="#">
        <span class="logo mr-2"></span>
        <span>TodoList</span>
      </a>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item">
            <router-link class="nav-link" to="/add">待办事项</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/done">已完成</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/delete">已删除</router-link>
          </li>
        </ul>
      </div>
    </nav>
    <div class="container">
      <router-view></router-view>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Home'
})
</script>

<style lang="scss" scoped>
.container {
  .logo {
    display: inline-block;
    width: 40px;
    height: 40px;
    background: url('~@/assets/logo.png') center center no-repeat;
    background-size: contain;
  }
}
</style>
