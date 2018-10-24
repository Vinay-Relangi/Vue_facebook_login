<template>
   <header>
      <div class="container">
         <div class="row">
            <div class="col-sm-6">
               <div class="logo">FACEBOOK</div>
            </div>
            <div class="col-sm-6 hidden-xs">
               <div class="row">
                  <div class="col-sm-5">
                     <div class="form-group">
                        <input type="text" class="form-control no-border" placeholder="Email or Phone" name="email" v-model="username" />
                        <div class="login-bottom-text checkbox hidden-sm">
                           <label>
                           <input type="checkbox" />
                           Keep me sign in
                           </label>
                        </div>
                     </div>
                  </div>
                  <div class="col-sm-5">
                     <div class="form-group">
                        <input type="text" class="form-control no-border" placeholder="Password" name="password" v-model="password" />
                        <div class="login-bottom-text hidden-sm"> Forgot your password? </div>
                     </div>
                  </div>
                  <div class="col-sm-2">
                     <div class="form-group">
                        <input type="button" value="login" class="btn btn-primary btn-header-login" v-on:click="onSubmit" />
                     </div>
                  </div>
               </div>
            </div>
         </div>
      </div>
   </header>
</template>

<script>
import router from '../../router'
export default {
    data () {
        return {
            username: '',
            password: ''
        }
    },
  methods: {
    onSubmit:function (event){
		console.log(event);
		if(this.username && this.password){
			this.usename ='';
			this.password = '';
			localStorage.setItem('user',this.username);
			router.push('home');
		}
    }
  }
};
</script>