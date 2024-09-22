<template>
  <el-row>
        <el-col :span="5">
            <el-text>商品名称：</el-text>
            <el-input v-model="search.GoodsName" style="width: 170px" placeholder="请输入商品名称" clearable />
        </el-col>
        <el-col :span="6">
            <el-text>创建日期：</el-text>
            <el-date-picker v-model="search.CreateTime" type="date" placeholder="选择创建日期" value-format="YYYY-MM-DD" />
        </el-col>
        <el-col :span="3">
            <el-button type="primary" @click="handleGetGoodsList">查询</el-button>
        </el-col>
    </el-row>
  <el-table :data="tableData" style="width: 100%">
    <el-table-column prop="date" label="Date" width="180" />
    <el-table-column prop="name" label="Name" width="180" />
    <el-table-column prop="address" label="Address" />
  </el-table>
</template>

<script lang="ts" setup>
const tableData = [
  {
    date: '2016-05-03',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
  {
    date: '2016-05-02',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
  {
    date: '2016-05-04',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
  {
    date: '2016-05-01',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
]
</script>
