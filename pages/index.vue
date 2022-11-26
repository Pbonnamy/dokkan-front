<template>
  <h1>Index page</h1>
</template>
<script>
export default {
  name: 'Index',
  data() {
    return {
    };
  },
  mounted() {
    this.checkHealth();
  },
  methods: {
    async checkHealth() {  
      const response = await $fetch( 'http://127.0.0.1:8000/api/health', {
        method: 'GET',
      });

      console.log(response);
    }
  },
};
</script>