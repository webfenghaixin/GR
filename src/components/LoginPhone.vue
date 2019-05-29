<template>
    <div>
    <div class="login-bg" style="background:url('img/load_bg.jpg')">
        <div class="login-w">
            <div class="form-box">
                <form>
                    <h3>手机号登录</h3>
                    <div class="form-item-i">
                        <div class="form-item-t">
                            <input type="text" placeholder="请输入手机号">
                        </div>
                        <div class="form-item-b">
                            <input type="text" placeholder="请输入验证码">
                            <input type="button" value="验证码">
                        </div>
                    </div>
                    <div class="form-item-t">
                        <button>登录</button>
                    </div>
                    <div class="form-item-a">
                            <router-link to="/Login" href="">用户名密码登录</router-link>
                        <div>
                            <router-link to="/UserReg" href="">注册</router-link>
                            <a href="#">忘记密码?</a>
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            uname:"",
            upwd:"",
            msg:""
        }
    },
    methods:{
        login(){
            var u=this.uname;
            var p=this.upwd;
            var sql=`login?uname=${u}&upwd=${p}`;
            this.axios.get(sql).then(result=>{
                this.msg=result.data.data;
                if(result.data.code==1){
                    setTimeout(()=>{
                        this.$router.push("Index");
                    },1000);
                }
                
            })
        }
    }
}
</script>

<style scoped>
    
    .login-bg{
        width: 100%;
        background-size: cover;
    }
    .login-w{
        height: 772px;
        position: relative;
        width: 1200px;
        margin: 0 auto;
    }
    .form-box{
        width: 500px;
        padding: 0 50px 50px 50px;
        background:rgba(255,255,255,0.6);
        position: absolute;
        top:243px;
        left:350px;
    }
    .form-box h3{
        display: block;
        text-align: center;
        font-size:23px;
        font-weight: 400;
        padding: 50px 0;
    }
    a{
    text-decoration: none !important;
}
    .form-item-t input{
        display: block;
        padding-left:35px;
        background:url('../img/phone.png') no-repeat;
        background-color: #fff;
        width: 461px;
        height: 30px;
        border:1px solid #a9a9a9;
        margin-bottom: 20px;
    }
    .form-item-b input:first-child{
        display: inline-block;
        height: 34px;
        width: 70%;
        box-sizing: border-box;
    }
    .form-item-b input:last-child{
        display: inline-block;
        width: 29%;
        height: 34px;
        background: #cfb2f6;
        color:#fff;
        box-sizing: border-box;
        margin-bottom: 20px;
    }
    .form-item-t>button{
        display:block;
        width: 100%;
        margin: 0 auto;
        height: 38px;
        background: #cfb2f6;
        font-size: 18px;
        color:#fff;
    }
    .form-item-a{
        margin-top: 10px;
    }
    .form-item-a>a{
        float: left;
    }
    .form-item-a>div{
        text-align: right;
    }
    .form-item-a>div>a:first-child{
       margin-right:10px;
    }
</style>




