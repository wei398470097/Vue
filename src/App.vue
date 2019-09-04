<template>
  <div id="app">
    <router-view v-wechat-title="$route.meta.title"/>
  </div>

</template>
<script>
  export default {

  }
  //App接口
  window['setAppInfo'] =function (uid,os) {
    window.os=os
    window.uid=uid
  }
  //H5接口
  window.addEventListener('message',function(event){
    let data = event.data
    if(data.os !== undefined){
      window.os=data.os
      window.uid=data.uid
    }
  },false)
</script>
<style lang="stylus" rel="stylesheet/stylus">
  body,html
    background #fff;
</style>
