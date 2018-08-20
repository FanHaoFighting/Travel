<template>
  <div>
    <div class="title">热门推荐</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of list"
        :key="item.id"
      >
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
  /* data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1609/f1/f10a167617911cb6a3.water.jpg_200x200_c50e0aed.jpg',
        title: '合肥万达水上乐园',
        desc: '合肥万达水乐园，浪漫的水上乐园'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1609/a9/a90f734bbc7b80aea3.water.jpg_200x200_fac101cb.jpg',
        title: '合肥海洋世界',
        desc: '合肥海洋世界，浪漫的海底世界'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/a5/a50187e22a0c3fac0.water.jpg_200x200_a8c97c3b.jpg',
        title: '合肥万达文旅城',
        desc: '合肥万达文旅城，文化旅游'
      }]
    }
  } */
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
    .item-button
      line-height: .44rem
      margin-top: .16rem
      background: #ff9300
      padding: 0 .2rem
      border-radius: .06rem
      color: #fff
</style>
