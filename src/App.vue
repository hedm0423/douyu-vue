<template>
    <div class="container">
      <router-view></router-view>
      <sidebar :show.sync="show"></sidebar>
    </div>
</template>

<script>
import Sidebar from './components/sidebar'

export default {
  data(){
    return {
      show:false
    }
  },
  components: {
    Sidebar
  },
  events: {
    'showNav':function(){
      this.show=true;
    }
  }
}
</script>

<style lnag='scss'>
@import './assets/styles/icon.css';
@import './assets/styles/reset.css';
@import './assets/styles/video-js.css';
body{
  background-color: #ebebeb;
  height: 100%;
}
*{
  box-sizing: border-box;
}
img{
  width: 100%; 
  transition: opacity 1.2s ease; 
  opacity: 1;
}
</style>
