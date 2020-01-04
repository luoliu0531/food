<template>
  <div>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/1.png" />
        </i-grid-icon>
        <i-grid-label>中餐</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/2.png" />
        </i-grid-icon>
        <i-grid-label>西餐</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/3.png" />
        </i-grid-icon>
        <i-grid-label>小吃</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/4.png" />
        </i-grid-icon>
        <i-grid-label>饮料</i-grid-label>
    </i-grid-item>
  </i-grid>
  <i-panel :title=" title_name">
    <view style="padding: 15px;">
      <i-card title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
        <view slot="content">内容不错</view>
        <view slot="footer">尾部内容</view>
    </i-card>
    <i-card title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
        <view slot="content">内容不错</view>
        <view slot="footer">尾部内容</view>
    </i-card>
    <i-card title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
        <view slot="content">内容不错</view>
        <view slot="footer">尾部内容</view>
    </i-card>
  </view>
  </i-panel>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title_name: "热门",
      grids:[
        {title:"中餐",image:"/static/images/1.png"},
        {title:"西餐",image:"/static/images/2.png"},
        {title:"小吃",image:"/static/images/3.png"},
        {title:"饮料",image:"/static/images/4.png"},
      ]
    }
  },

  methods: {
  },

  created () {
  }
}
</script>

<style scoped>
</style>
