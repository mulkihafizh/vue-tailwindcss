<template>
  <Navbar />
  <Head />
</template>
<script>
import Navbar from "./components/Navbar.vue";
import Head from "./components/Head.vue";
export default {
  name: "App",
  components: {
    Navbar,
    Head,
  },
};
</script>
