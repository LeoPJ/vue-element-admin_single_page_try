<template>
  <div>
    <el-row>
      <el-col :span="2">
        <img src="http://eic.hust.edu.cn/professor/wenhao/index.files/wenhao_14436_image002.png" class="image">
      </el-col>
      <el-col :span="22">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span>福神</span>
          </div>
          <div class="text item">
            爷最牛批
          </div>
        </el-card>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="2">
        <img src="http://eic.hust.edu.cn/professor/wenhao/index.files/wenhao_14436_image002.png" class="image">
      </el-col>
      <el-col :span="22">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span>福神</span>
          </div>
          <div class="text item">
            爷最牛批
          </div>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
// export default {
//   data() {
//     return {
//       currentDate: new Date()
//     }
//   }
// }
// </script>

<style scoped>
  .el-row {
    margin-left: 30px;
	margin-right: 30px;
    margin-top: 20px;
  }

  .el-col {
    border-radius: 4px;
  }

  .text {
    font-size: 14px;
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
