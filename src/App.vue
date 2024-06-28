<template>
  <div class="app">
    <!-- 1.区域header -->
    <area-header :title="hightScore.title" :subtitle="hightScore.subtitle" />

    <!-- 2.房间列表 -->
    <div class="room-list">
      <template v-for="item in hightScore.list" :key="item.id">
        <room-item :item-data="item" />
      </template>
    </div>
  </div>
</template>

<script setup>
import AreaHeader from './components/AreaHeader'
import RoomItem from './components/RoomItem.vue'
//1.获取数据
import hightScore from './data/high_score.json'
// console.log(hightScore);


</script>

<style lang="less" scoped>
.app {
  width: 1032px;
  padding: 40px;
  margin: 0 auto;
}

.room-list {
  display: flex;
  flex-wrap: wrap;
  margin: 10px -8px;
}
</style>