<template>
  <div class="home">
    <AMANAMAN msg></AMANAMAN>
  </div>
</template>

<script>
// @ is an alias to /src

import AMANAMAN from "@/components/AMANAMAN.vue";
export default {
  name: "HomeView",
  components: {
    AMANAMAN,
  },
};
</script>
