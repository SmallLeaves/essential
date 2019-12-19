<template>
  <div class="navbar navbar-default topnav">
    <div class="container">
      <div class="navbar-header">
        <a href="/" class="navbar-brand">
          <span class="title">{{ logo.title }}</span>
          <img :src="logo.src" :alt="logo.title">
        </a>
      </div>

      <div id="top-navbar-collapse" class="collapse navbar-collapse">
        <ul class="nav navbar-nav">
          <!-- :class="{ active: index === activeNavIndex }" -->
          <li v-for="(item,index) in navList" :key="index" :class="{active:index === activeNavIndex}">
            <a href="#" @click="changeNavIndex(index)">{{ item }}</a>
          </li>
        </ul>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'TheHeader',
  data() {
    return {
      logo: {
        src: `https://avatars3.githubusercontent.com/u/26822418?s=460&v=4`,
        title: 'Title'
      },
      navList: ['aaa', 'sss', 'ddd', 'ddd'],
      activeNavIndex: 0
    }
  },
  beforeCreate() {
    this.uploadsUrl = 'https://cdn.learnku.com/uploads/'
  },
  methods:{
    changeNavIndex(index){
      this.activeNavIndex = index
    }
  }
}
</script>

<style>
  @import "../../../static/styles/header.css";
  .active{
    background: yellow;
  }
</style>
