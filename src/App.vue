<template>
  <div id="app">
    <router-view class="slideInRight" />
  </div>
</template>

<script>
  export default {
    name: 'App'
  }
</script>

<style lang="less">
  @import '~vux/src/styles/reset.less';

  #app {
    height: 100%;
    background: #F3EEEB;
    .vux-header {
      background: white;
      color: #231815 !important;
      .vux-header-title {
        font-size: .426667rem;
        color: #231815 !important;
      }
    }
    @keyframes slideInRight {
      from {
        -webkit-transform: translate3d(100%, 0, 0);
        transform: translate3d(100%, 0, 0);
        /* visibility: visible; */
      }

      to {
        -webkit-transform: translate3d(0, 0, 0);
        transform: translate3d(0, 0, 0);
      }
    }

    .slideInRight {
      -webkit-animation-name: slideInRight;
      animation-name: slideInRight;
      -webkit-animation-duration: .4s;
      animation-duration: .4s;
    }
  }

</style>
