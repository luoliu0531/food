<template>
  <div>
    <i-grid>
    <i-grid-item @click="goType(grid)" v-for="grid in grids" :key="grid">
        <i-grid-icon>
            <image :src="grid.image" />
        </i-grid-icon>
        <i-grid-label>{{grid.title}}</i-grid-label>
    </i-grid-item>
  </i-grid>
  <i-panel :title=" title_name">
    <view style="padding: 15px;">
      <i-card v-for="item in top" :key="item" :extra="item.name" :thumb="item.image">
        <view slot="content">{{item.remark}}</view>
        <view slot="footer">{{item.address}}</view>
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
      ],
      top:[
        {name:"小重庆",address:"武昌区团结大道318号",image:"cloud://ll-1zrro.6c6c-ll-1zrro-1301063015/小重庆.jpg",remark:"环境舒适宜人，味道可口"},
        {name:"秀玉红茶坊",address:"武昌区徐东大街18号销品茂4F层",image:"cloud://ll-1zrro.6c6c-ll-1zrro-1301063015/秀玉红茶坊.jpg",remark:"品种齐全，服务良好"},
        {name:"一点点",address:"友谊大道三角花园6号地块C2-2",image:"cloud://ll-1zrro.6c6c-ll-1zrro-1301063015/一点点.jpg",remark:"奶茶很好喝"},
        {name:"仟吉",address:"武昌区友谊大道396号国际城福客茂1层",image:"cloud://ll-1zrro.6c6c-ll-1zrro-1301063015/仟吉.jpg",remark:"人气很旺的面包店"}
      ]
    }
  },

  methods: {
    goType(type){
       console.log(type) 
       let url = '../list/main?type=' + type.title
       mpvue.navigateTo({ url })
    }
  },

  created () {
  }
}
</script>

<style scoped>
</style>
