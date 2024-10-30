<template>
  <div>
    <nav class="navbar navbar-expand-lg bg-body-tertiary ">
      <div class="container-fluid">
        <img src="@/assets/img/people.png" alt="" class="avator"><a class="navbar-brand" href="#">我的超级无敌简历</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation" @click="showBiao">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">个人简介</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Link</a>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                aria-expanded="false">
                Dropdown
              </a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Action</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
                <li>
                  <hr class="dropdown-divider">
                </li>
                <li><a class="dropdown-item" href="#">Something else here</a></li>
              </ul>
            </li>
            <li class="nav-item">
              <a class="nav-link disabled" aria-disabled="true">Disabled</a>
            </li>
          </ul>
          <form class="d-flex" role="search">
            <input class="form-control me-2" type="search" placeholder="搜索" aria-label="Search" v-model="inptValue">
            <button class="btn btn-outline-success" type="button" @click="submit"><span>搜索</span></button>
          </form>
        </div>
      </div>
    </nav>
    <div class="container-sm">100% wide until small breakpoint</div>
    <div class="container-md">100% wide until medium breakpoint</div>
    <div class="container-lg">100% wide until large breakpoint</div>
    <div class="container-xl">100% wide until extra large breakpoint</div>
    <div class="container-xxl">100% wide until extra extra large breakpoint</div>

  </div>
</template>
<script setup>
import { ref } from 'vue';
const inptValue = ref("")
const show = ref(false)
const submit = function () {
  console.log(inptValue.value);
}
const showBiao = () => {
  let collapse = new bootstrap.Modal(document.getElementById('exampleModal'))
  show.value != show.value
  console.log(collapse.value);

}
</script>
<style scoped lang="scss">
@import "@/style/_variables.scss";
@import "@/style/global.scss";

.avator {
  @include avator;
}

.navbar-brand {
  color: black;
}
</style>