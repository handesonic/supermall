<template>
  <div class="wrapper" ref="wrapper">
    <div class="content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'

export default {
  data() {
    return {
      scroll: null
    }
  },
  mounted() {
    // this.scroll = new BScroll(this.$refs.wrapper,{
    //   click: true,
    //   disableTouch: false
    // })
    // this.scroll.refresh()
    this.$nextTick(() => {
        if (!this.scroll) {
          this.scroll = new BScroll(this.$refs.wrapper, {
          })
        }else {
          this.scroll.refresh()
        }
      })
    // setTimeout(()=>{
    //   this.scroll = new BScroll(this.$refs.wrapper,{
    //     click: true,
    //     disableTouch: false
    //   });
    // },20)
  }
}
</script>

<style>

</style>