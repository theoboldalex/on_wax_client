<template>
  <div class="container">
    {{ records }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      records: []
    };
  },
  async mounted() {
    this.records = await this.$axios.$get(
      "http://localhost:5000/api/v1/records/user/2"
    );
  }
};
</script>

<style></style>
