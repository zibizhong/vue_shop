<template>
  <div class="login-warp">
    <div class="ms-title">Music后台管理登录</div>
    <div class="ms-login">
      <el-form ref="ruleform" :model="form" label-width="80px">
        <el-form-item label="用户名">
          <el-input v-model="form.username"></el-input>
        </el-form-item>
        <el-form-item label="密码">
          <el-input
            v-model="form.userpwd"
            type="password"
            aria-required="required"
          ></el-input>
        </el-form-item>
        <el-form-item>
          <el-button type="primary" @click="onSubmit">登录</el-button>
          <el-button type="primary" @click="reset">重置</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>
<style>
.login-warp {
  background: url("../assets/233639-16293873999da5.jpg");
  width: 100%;
  height: 100%;
  position: absolute;
  background-size: cover;
}
.ms-title {
  position: absolute;
  top: 50%;
  width: 100%;
  margin-top: -230px;
  font-size: 30px;
  font-weight: 600;
  text-align: center;
  color: #fff;
}
.ms-login {
  position: absolute;
  left: 50%;
  top: 50%;
  width: 300px;
  height: 160px;
  margin-left: -150px;
  margin-top: -150px;
  padding: 40px;
  border-radius: 5px;
  background-color: #fff;
}
</style>
<script>
export default {
  data () {
    return {
      form: {
        username: '',
        userpwd: ''
      }
    }
  },
  methods: {
    onSubmit () {
      console.log('submit!')
    },
    reset () {
      this.username = null
      this.userpwd = null
    }
  }
}
</script>
