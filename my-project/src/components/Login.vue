<template>
  <div class="hello">
    <h2>登录</h2>
    <div>
       <input type="text" placeholder="Email" v-model="account">
       <input type="password" placeholder="Password"  v-model="password">
       <a href="javascript:;" class="log-btn" @click="login">Login</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data () {
    return {
      account: '',
      password: ''
    }
  },
  methods:{
    //登录逻辑
      	login(){
      		if(this.account==''){
      			alert("邮箱不能为空");
      		}else if(this.password==''){
      		  alert("密码不能为空");
      		}
      	}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2 {
  font-weight: normal;
  color:#35495E;
}
input {
  display: block;
  width:300px;
  position: relative;
  left:50%;
  transform:translate(-50%);
  margin-top:18px;
  height:25px;
  -webkit-border-radius: 5px;
}
.log-btn{
  width:300px;
  display: block;
  text-align: center;
  line-height: 50px;
  margin:20px auto ;
  height:40px;
  color:#fff;
  font-size:13px;
  -webkit-border-radius: 5px;
  background-color: #41B883;
}
</style>
