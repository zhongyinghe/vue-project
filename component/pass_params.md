1、关于element ui在表格的列中下拉组件command传输对象的方式(省略一些代码)
```
<template slot-scope="scope">
  <el-dropdown>
    <el-dropdown-item :command='{id:scope.row.id,status: 1}'>通过</el-dropdown-item>
  </el-dropdown>
</template>
```
