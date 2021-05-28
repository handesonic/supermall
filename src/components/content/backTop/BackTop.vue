<template>
  <div class="back-top" @click="backClick">
    <img src="~assets/img/common/top.png" alt="">
  </div>
</template>

<script>
export default { 
  methods: {
    backClick() {
      // .animate({'scrollTop':0},100);
      let body = document.documentElement || document.body
      body.scrollTo({
        top: 0,
        behavior: "smooth"
      });
      // document.documentElement.scrollTop = 0;
      // console.log(document.documentElement.scrollTop)
    }
  }
}
</script>

<style>
  .back-top{
    position: fixed;
    right: 8px;
    bottom: 55px;
  }
  .back-top img{
    width: 43px;
    height: 43px;
  }
</style>