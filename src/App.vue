<template>
  <router-view :key="$route.path" />
</template>

<script>
import "bootstrap/dist/css/bootstrap.min.css";
export default {
  data() {
    return {
      inHeight: document.querySelector("body"),
      wHeight: window.innerHeight,
      height: 0,
    };
  },
  mounted() {
    document.title = "Anasayfa | ERDEM HAMZA";
    this.height = window.innerHeight;
  },
  methods: {
    resizeHandler() {
      this.height = window.innerHeight;
      document.querySelector("body").style.height = this.height + "px";
    },
  },
  created() {
    window.addEventListener("resize", this.resizeHandler);
    window.addEventListener("DOMContentLoaded", this.resizeHandler, {
      once: true,
    });
  },
  destroyed() {
    window.removeEventListener("resize", this.resizeHandler);
  },
};
</script>

<style>
@font-face {
  font-family: Everett-Regular;
  src: url("assets/fonts/Everett-Regular.otf") format("opentype");
}

@font-face {
  font-family: Everett-Regular;
  font-weight: bold;
  src: url("assets/fonts/Everett-Regular.otf") format("opentype");
}
#app {
  font-family: Everett-Regular, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  font-family: Everett-Regular;
  transition: all 300ms ease;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

* {
  scroll-behavior: smooth;
}

@media (max-width: 576px) {
  .py-xs-4 {
    padding-top: 1.5rem !important;
    padding-bottom: 1.5rem !important;
  }
  .px-xs-4 {
    padding-left: 1.5rem !important;
    padding-right: 1.5rem !important;
  }
  .pl-xs-4 {
    padding-left: 1.5rem !important;
  }
  .h-xs-50 {
    height: 50% !important;
  }
  .h-xs-100 {
    height: 100% !important;
  }
  body .owl-prev,
  body .owl-next {
    top: 47%;
    width: 40px;
    height: 40px;
  }
  .mb-n20 {
    margin-top: -20px;
  }
  .lead {
    font-size: 9px;
    margin-top: 4.2rem;
  }
  .ul-fontsize a,
  .ul-fontsize address {
    font-size: 9px;
    margin-bottom: 0;
  }
  .w-xs-50 {
    width: 50% !important;
  }
  .mb-xs-1 {
    margin-bottom: 0.3rem !important;
  }
  .justify-content-sm-end {
    justify-content: flex-end;
  }
}

body {
  font-family: Everett-Regular;
  width: 100%;
}

a,
a:hover {
  text-decoration: none;
  color: inherit;
  font-family: inherit;
}

.responsive-fs {
  font-size: calc(0.5rem + 2vw);
}

.responsive-fs_project {
  font-size: calc(0.5rem + 1.5vw);
}

h1 {
  margin-bottom: 0;
}

.z-51 {
  z-index: 51;
}

.hv-100 {
  height: 100vh;
}

.hv-50 {
  height: 50vh;
}

.top-bar,
.bottom-bar {
  position: fixed;
  z-index: 55;
}

.top-bar {
  top: 0;
}

.bottom-bar {
  bottom: 0;
}

.lh-1 {
  line-height: 1;
}

.a-black {
  color: #000 !important;
}

.a-black a {
  color: #000 !important;
}

.text-black {
  color: #000 !important;
}

.filter-black {
  filter: invert(100%);
}

.hm-100 {
  min-height: 100vh;
}

/* VIDEO */
.video-bg {
  position: absolute;
  height: 100%;
  width: 100%;
  left: 0;
  top: 0;
  z-index: -5;
  object-fit: cover;
}
.video-bg::after {
  content: "";
  display: block;
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  z-index: 2;
}

.z-51 {
  z-index: 51;
}

.h-fit {
  height: fit-content;
}

.logo-holder img {
  width: calc(8rem + 10vw);
}

.middle-logo img {
  width: calc(8rem + 10vw);
}

.has-background {
  position: relative;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  /* box-shadow: inset 0px 0px 20px 20px #000000ab; */
  transition: all 200ms;
}

.has-background::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 5;
  background-color: rgba(0, 0, 0, 0.25);
}

.has-background a {
  position: relative;
  z-index: 10;
}

.bg-projects {
  overflow: hidden;
}

.has-background:hover {
  background-size: cover;
}

.slick-arrow {
  position: absolute;
}
.prev-btn {
  left: 10%;
  transform: rotate(45deg);
}
.next-btn {
  right: 10%;
  transform: rotate(225deg);
}
.prev-btn,
.next-btn {
  top: 43%;
  border-left: 1px solid #fff;
  border-bottom: 1px solid #fff;
  border-right: none;
  border-top: none;
  background: transparent;
  z-index: 70;
  width: 120px;
  height: 120px;
}
.line-height-5 {
  line-height: 0.9;
}
.page {
  cursor: url("https://demo.maharethane.com/erdem-hamza8/img/view-project-100.png"),
    auto;
}
</style>
