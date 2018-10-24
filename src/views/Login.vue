<template>
<div>
	<LoginHeader/>
	<LoginContent/>
	<LoginFooter/>
</div>
</template>

<script>
import LoginHeader from "../components/login/LoginHeader.vue";
import LoginContent from "../components/login/LoginContent.vue";
import LoginFooter from "../components/login/LoginFooter.vue";

export default {
  name: "Login",
  components: {
    LoginHeader,
    LoginContent,
    LoginFooter
  }
};
</script>