<template>
	<header/>
	<content/>
	<!-- <Footer/> -->
</template>

<script>
import header from "./header.vue";
import content from "./content.vue";
import Footer from "./footer.vue";

export default {
  name: "login",
  props: {
    msg: String
  }
};
</script>

<style scoped>
</style>
