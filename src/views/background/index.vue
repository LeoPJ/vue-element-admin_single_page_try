<template>
  <div>
    <el-row>
      <el-card class="box-card">
        <h1>这是标题 1</h1>
        <h2>这是标题 2</h2>
        <h3>这是标题 3</h3>
        <h4>这是标题 4</h4>
        <h5>这是标题 5</h5>
        <h6>这是标题 6</h6>
      </el-card>
    </el-row>
  </div>
</template>

<style>
  .el-row {
    margin-left: 30px;
	margin-right: 30px;
    margin-top: 20px;
  }
  .el-col {
    border-radius: 4px;
  }
  .text {
    font-size: 114px;
  }

  .item {
    margin-bottom: 18px;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }

  .box-card {
    width: 100%;
  }
</style>
