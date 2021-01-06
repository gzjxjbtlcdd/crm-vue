<template>
  <div class="entity-box">
    <!--  操作的部分-->
    <div class="execute-box">
      <!--    size：表示大小 size 尺寸 string medium/small/mini
              type：表示按钮的颜色 primary/success/Warning/danger/info/text
              plain：镂空颜色
              round：button是否是圆角显示-->
      <el-button-group>
        <el-button size="mini" type="primary">新建</el-button>
        <el-button size="mini" type="danger">批量删除</el-button>
      </el-button-group>
    </div>
    <!--  表单查询
    搜索表单 预留
    -->
    <div class="search"></div>
    <!--  表单数据 数据展示-->
    <!-- tooltip-effect="light" 给隐藏信息...设置颜色-->
    <div class="table-box">
      <el-table
          stripe
          :data="tableData"
          tooltip-effect="light"
          border="true"
          style="width: 100%">
        <el-table-column
            align="center"
            type="selection"
            width="55">
        </el-table-column>
        <el-table-column
            align="center"
            prop="date"
            label="日期"
        >
        </el-table-column>
        <el-table-column
            align="center"
            prop="name"
            label="姓名"
        >
        </el-table-column>
        <!--     show-overflow-tooltip 信息超出 ...隐藏   -->
        <el-table-column
            align="center"
            prop="address"
            label="地址"
            show-overflow-tooltip>
        </el-table-column>
        <el-table-column
            align="center"
            label="操作"
        >
          <!--这种方式是可以展示的但是无法取值（
          必须把按钮添加在 template标签）-->
          <template>
            <el-button size="mini" type="primary">编辑</el-button>
            <el-button size="mini" type="danger">删除</el-button>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <!--  分页插件-->
    <div class="page-box">
      <el-pagination
          background
          layout="prev, pager, next"
          :total="1000">
      </el-pagination>
    </div>
  </div>
</template>

<script src="./index.js">

</script>

<style scoped lang="less" src="./index.less">

</style>