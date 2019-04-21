<template>
  <div id="login-container">
    <div class="login-box">
      <el-form ref="loginFormRef" :model="loginForm">
        <el-form-item label>
          <el-input v-model="loginForm.name"></el-input>
        </el-form-item>
        <el-form-item label>
          <el-input v-model="loginForm.password"></el-input>
        </el-form-item>
        <el-row>
          <el-col :offset="15">
            <el-button type="primary">登录</el-button>
            <el-button type="info">重置</el-button>
          </el-col>
        </el-row>
      </el-form>
      <div class="avatar-box">
        <img src="../assets/img/logo.png" alt>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      loginForm: {
        name: '',
        password: ''
      }
    }
  }
}
</script>

<style lang="less" scoped>
#login-container {
  background-color: #2b4b6b;
  height: 100%;
  // overflow: hidden;
  .login-box {
    width: 450px;
    height: 304px;
    background-color: #fff;
    border-radius: 4px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    .el-form {
      position: absolute;
      bottom: 0;
      width: 100%;
      padding: 20px;
      box-sizing: border-box;
    }
    .avatar-box {
      width: 130px;
      height: 130px;
      border: 1px solid #eee;
      border-radius: 50%;
      padding: 8px;
      box-shadow: 0 0 10px #eee;
      position: absolute;
      left: 50%;
      transform: translate(-50%, -50%);
      background-color: #fff;
      img {
        width: 100%;
        height: 100%;
        border-radius: 50%;
        background-color: #eee;
      }
    }
  }
}
</style>
