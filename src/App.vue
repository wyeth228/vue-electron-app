<template>
  <component :is="layout">
    <router-view />
  </component>
</template>

<script>
import DefaultLayout from "@/layouts/default.layout.vue";

export default {
  components: {
    DefaultLayout,
  },
  mounted() {
    this.$router.push("/user");
  },
  computed: {
    layout() {
      return (this.$route.meta.layout || "default") + "-layout";
    },
  },
};
</script>
