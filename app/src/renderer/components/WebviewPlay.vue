<template>
  <div>
    <webview
      :src="url"
      class="webview"
      plugins="true"
    ></webview>
  </div>
</template>

<script>
  export default {
    name: 'webview-play',
    created () {
      console.log(22222)
      console.log(this.$route.query.url)
      this.url = `http://000o.cc/jx/ty.php?url=${this.$route.query.url}`
      // this.url = 'http://www.5ifxw.com/vip/'
    }
  }
</script>

<style scoped>
  img {
    margin-top: -25px;
    width: 450px;
  }

  .webview {
    width: 100vw;
    height: calc(100vh - 30px);
    position: absolute;
    top: 30px;
    left: 0;
  }

  .nav {
    position: absolute;
    top: 0;
    left: 0;
    height: 30px;

    input {
      width: 100%;
    }
  }

  button {
    position: fixed;
    top: 50%;
    z-index: 1000;
  }
</style>
