<template>
  <div class="container">
    <div class="container_img">
      <div style="height: 100%">
        <div class="userlogo">
          <img src="../assets/userlogo.jpg" alt="">
          <header class="header">登录</header>
        </div>
        <div class="content">
          <van-form @submit="onSubmit">
            <van-field
              v-model="username"
              left-icon="user-circle-o"
              right-icon="warning-o"
              :rules="[{ required: true, message: '请填写用户名' }]"
            />
            <van-field
              v-model="password"
              type="password"
              left-icon="passed"
              right-icon="warning-o"
              :rules="[{ required: true, message: '请填写密码' }]"
            />
            <div style="margin: 16px;">
              <van-button round block type="info" native-type="submit">
                登录
              </van-button>
            </div>
          </van-form>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      username: '18813007814',
      password: '123456'
    }
  },
  computed: {

  },

  methods: {
    onSubmit (values) {
      console.log('submit', values)
    }
  }
}
</script>
<style scoped lang="scss">
  .container .userlogo {
    margin-top: 80px;
    text-align: center;
  }
  .container .userlogo img {
    margin: 0 auto;
    width: 120px;
    height: 120px;
    border-radius: 50%;
  }
  .container .container_img {
    width: 100%;
    height: 100%;
    position: fixed;
    z-index: -10;
    background-image:url("../assets/logimg.jpg");
    background-repeat: no-repeat;
    background-position: 0px 0px;
    background-size: 100% 100%;
  }
  .container .header {
    padding: 20px;
    text-align: center;
    font-size: 22px;
    font-family:"Times New Roman",Georgia,Serif
  }
  .container .content {
    padding: 20px;
  }
</style>
