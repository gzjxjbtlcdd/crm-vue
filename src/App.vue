<template>
  <!--  template 这个htm15当中的模板标签 这个标签中的内容  默认是不显示的
         应用只有一个页面 index.html App.vue 这里面的内容  就是显示在 index，htm1当中的
         template中的内容拿到放到index,html中展示
         template模板标签中 只能有一个根标签

         .Vue 后级名的文件 是vue的组件文件 这个文件中包含三块信息
                template：页面的 html
                script：编写js的
                sty1e： 编写这个页面的样式的

         router-view：这个标签表示的一个不确定显示的内容 这个要显示的内容一个vue的组件  并且在 router中配置路径才能显示
  -->
  <div class="app-box">
    <router-view/>
  </div>

</template>

<style lang="less">
* {
  margin: 0;
  padding: 0;
}
html,body,.app-box{
  width: 100%;
  height: 100%;
}
</style>
