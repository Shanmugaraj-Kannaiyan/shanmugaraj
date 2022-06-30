<template>


    <div class="container">
<!-- Pills navs -->
<ul class="nav nav-pills nav-justified mb-4 " id="ex1" role="tablist">
  <li class="nav-item" role="presentation">
    <a class=" nav-link active " id="tab-login" data-mdb-toggle="pill" href="/" role="tab"
      aria-controls="pills-login" aria-selected="true">Login</a>
  </li>
  <li class="nav-item" role="presentation">
    <nuxt-link class="nav-link " id="tab-register" data-mdb-toggle="pill" to="/register" role="tab"
      aria-controls="register" aria-selected="false">Sign up</nuxt-link>
  </li>
</ul>
<!-- Pills navs -->

<!-- Pills content -->
<div class="tab-content">
  <div class="tab-pane fade show active" id="login" role="tabpanel" aria-labelledby="tab-login">
    <form>
      <div class="text-center mb-3">
        <!-- <p>Sign in with:</p> -->
        <!-- <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-facebook-f"></i>
        </button>

        <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-google"></i>
        </button>

        <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-twitter"></i>
        </button>

        <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-github"></i>
        </button> -->
      </div>

      <!-- <p class="text-center">or:</p> -->

      <!-- Email input -->
      <div class="form-outline mb-4">
        <input type="email" id="loginName" class="form-control" placeholder="Email or username"  v-model='name'>
        <label class="form-label" for="loginName"></label>
      </div>

      <!-- Password input -->
      <div class="form-outline mb-4">
        <input type="password" id="loginPassword" class="form-control" placeholder="Password" v-model="pwd">
        <label class="form-label" for="loginPassword"></label>
      </div>

      <!-- 2 column grid layout -->
      <div class="row mb-4">
        <div class="col-md-6 d-flex justify-content-center">
          <!-- Checkbox -->
          <div class="form-check mb-3 mb-md-0">
            <input class="form-check-input" type="checkbox" value="" id="loginCheck" checked />
            <label class="form-check-label" for="loginCheck"> Remember me </label>
          </div>
        </div>

        <div class="col-md-6 d-flex justify-content-center">
          <!-- Simple link -->
          <a href="#!" class="form-password">Forgot password?</a>
        </div>
      </div>

      <!-- Submit button -->
      <button type="submit" class="btn btn-primary btn-block mb-4 " id="signin" @click="login()">Sign in</button>

      <!-- Register buttons -->
      <div class="text-center">
        <p>Not a member? <nuxt-link to="/register" class="form-register">Sign up</nuxt-link></p>
      </div>
    </form>
  </div>
  <div class="tab-pane fade" id="pills-register" role="tabpanel" aria-labelledby="tab-register">
    <form>
      <div class="text-center mb-3">
        
        <!-- <p>Sign up with:</p> -->
        <!-- <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-facebook-f"></i>
        </button>

        <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-google"></i>
        </button>

        <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-twitter"></i>
        </button>

        <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-github"></i>
        </button> -->
      </div>

      <p class="text-center">or:</p>

      
</form>
</div>
</div>
</div> 

</template>

<script>
export default {
       data(){
         return{
           name:"",
           pwd:""
         }
       },
       methods:{
         login(){
           console.log('name',this.name,'pwd',this.pwd);
           if(this.name&&this.pwd){
                this.$nuxt.$router.push({path:'/demo?name='+this.name+'&password='+this.pwd})
            }else{
              alert('not filed')
            }
       
         }
       }
}
</script>

<style>
.container{
max-width:400px;
border:1px solid black;
background-color:white;
margin-top:90px;
border-radius:5px;
}
.form-register{
  text-decoration: none;
}
.form-password{
  text-decoration: none;
}
/* .btn{
  background-image: linear-gradient(to right, #fbc2eb 0%, #a6c1ee 51%, #fbc2eb 100%);
}
.btn:hover {
  background-position: right center !important; 
} */
/* .btn {
  flex: 1 1 auto;
  margin: 10px 0px 0px 110px;
  padding: 5px 40px;
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 200% auto;
 color: white; 

  box-shadow: 0 0 2px #eee;
 border-color: transparent !important;
   border-radius: 10px;
 } */
 /* #signin{
   margin-left: ;
 } */
/* .background{
  

} */
body{
 background:url('/images.jpeg') no-repeat;
 background-size:cover;
 


}
.nav-link {
    width: 100%;
    margin-top: 10px;
}
/* .btn{
  margin-left:130px ;
} */
html{
  height: 100%;
}
</style>