<template>
  <div class="container">
    <ul>
      <li>
        <v-link href="/">主页</v-link>
        <v-link href="/event">活动</v-link>
        <v-link href="/about">关于</v-link>
      </li>
    </ul>

    <slot></slot>
  </div>
</template>

<script>
  import VLink from '../components/VLink.vue'

  export default {
    components: {
      VLink
    }
  }
</script>

<style scoped>
  ul,li{
    list-style:none;
  }
  ul{padding-left:0;}
  .container {
    max-width: 600px;
    margin: 0 auto;
    padding: 15px 30px;
    background: #f9f7f5;
  }
  a{text-decoration:none;color:#000000;margin-right:10px;}
</style>
