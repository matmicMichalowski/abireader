<template>
  <div class="loader" aria-hidden="true">
    <div class="loader-inner ball-scale-ripple-multiple">
      <div></div>
      <div></div>
      <div></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Loader'
};
</script>

<style scoped>
@keyframes ball-scale-ripple-multiple {
  0% {
    -webkit-transform: scale(0.1);
    transform: scale(0.1);
    opacity: 1;
  }
  70% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0.7;
  }
  100% {
    opacity: 0;
  }
}

.ball-scale-ripple-multiple {
  position: relative;
  -webkit-transform: translateY(-25px);
  transform: translateY(-25px);
}
.ball-scale-ripple-multiple > div:nth-child(0) {
  -webkit-animation-delay: -0.8s;
  animation-delay: -0.8s;
}
.ball-scale-ripple-multiple > div:nth-child(1) {
  -webkit-animation-delay: -0.6s;
  animation-delay: -0.6s;
}
.ball-scale-ripple-multiple > div:nth-child(2) {
  -webkit-animation-delay: -0.4s;
  animation-delay: -0.4s;
}
.ball-scale-ripple-multiple > div:nth-child(3) {
  -webkit-animation-delay: -0.2s;
  animation-delay: -0.2s;
}
.ball-scale-ripple-multiple > div {
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: absolute;
  top: -2px;
  left: -26px;
  width: 50px;
  height: 50px;
  border-radius: 100%;
  border: 2px solid var(--main-color);
  -webkit-animation: ball-scale-ripple-multiple 1.25s 0s infinite
    cubic-bezier(0.21, 0.53, 0.56, 0.8);
  animation: ball-scale-ripple-multiple 1.25s 0s infinite
    cubic-bezier(0.21, 0.53, 0.56, 0.8);
}
</style>
