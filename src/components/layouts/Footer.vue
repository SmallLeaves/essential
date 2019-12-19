<template>
  <div id="footer">
    footer123
    <div v-title="asdasdasd">asdasdasd</div>
  </div>
</template>

<script>
  import title from '@/directives/title'

  export default{
    name: 'Footer',
    directives:{
      title
    }
  }
</script>

<style>
  #footer{
    position: absolute;
    bottom: 0;
    border-top: 3px solid #EEEEEE;
    display: block;
  }
</style>
