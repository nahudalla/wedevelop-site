<template>
  <div id="app">
    <router-view :scrollDuration="this.scrollDuration" />
  </div>
</template>

<script>
import Vue from 'vue'
import vueSmoothScroll from 'vue2-smooth-scroll'

Vue.use(vueSmoothScroll)

export default {
  name: 'app',
  data () {
    return {
      scrollDuration: 2000
    }
  }
}
</script>

<style>
  @font-face {
    font-family: 'Lato';
    src: url('assets/fonts/Lato-Light.ttf')  format('truetype');
    font-weight: 300;
  }

  @font-face {
    font-family: 'Lato';
    src: url('assets/fonts/Lato-Regular.ttf')  format('truetype');
    font-weight: 400;
  }

  @font-face {
    font-family: 'Lato';
    src: url('assets/fonts/Lato-Medium.ttf')  format('truetype');
    font-weight: 500;
  }

  @font-face {
    font-family: 'Lato';
    src: url('assets/fonts/Lato-Bold.ttf')  format('truetype');
    font-weight: 700;
  }

  @font-face {
    font-family: 'Lato';
    src: url('assets/fonts/Lato-Black.ttf')  format('truetype');
    font-weight: 900;
  }

  * {
    box-sizing: border-box;
  }

  #app {
    font-family: 'Lato', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
  }

  .highlight-paragraph {
    color: #272A40;
  }

  .alt-section {
    position: relative;
    background-color: #F7F9FC;
  }

  /* Cutted corners */
  .alt-section:before,
  .alt-section:after {
    content: "";
    position: absolute;
    width: 0;
    height: 0;
  }

  /* Top left cutted corner */
  .alt-section:before {
    top: 0;
    left: 0;
    border-bottom: 210px solid transparent;
    border-left: 240px solid #fff;
  }

  /* Bottom right cutted corner */
  .alt-section:after {
    bottom: 0;
    right: 0;
    border-bottom: 125px solid #fff;
    border-left: 170px solid transparent;
  }
</style>
