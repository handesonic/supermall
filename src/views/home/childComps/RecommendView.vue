<template>
  <div class="recommend">
    <div class="recommend-item" v-for="item in recommends" :key="item.index">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    recommends: {
      type: Array,
      default() {
        return []
      }
    }
  }
}
</script>

<style>
  .recommend {
    display: flex;
    text-align: center;
    font-size: 14px;
    padding: 10px 0;
    border-bottom: 8px solid #ddd;
  }
  .recommend-item {
    flex: 1;
  }
  .recommend-item img{
    width: 80px;
    height: 80px;
  }
</style>