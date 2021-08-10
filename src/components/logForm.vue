<template>
  <div class="login-container">
    <el-form class="login-form" ref="form" :model="user">
      <el-form-item >
        <el-input v-model="user.mobile"></el-input>
      </el-form-item>
      <el-form-item >
        <el-input v-model="user.code"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit">登录</el-button>
        <el-button>取消</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  name: 'logForm',
  props: {
    msg: String
  },
  data () {
    return {
      user: {
        mobile: '',
        code: ''
      }
    }
  },
  methods: {
    onSubmit () {
      console.log('submit!')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
  .login-container {
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    background: url('./img/surreal_art_2-wallpaper-1920x1080.jpg');
    background-size: cover;
    .login-form{
      background: #fff;
      padding: 50px;
      min-width: 300px;
      border-radius: 8px;
    }
  }

</style>
