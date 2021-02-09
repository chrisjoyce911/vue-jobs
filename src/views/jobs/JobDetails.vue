<template>
  <h1>{{ job.title }}</h1>
  <!-- gets an error if no data when trying to render -->
  <p>The job id is {{ id }}</p>
  <p>{{ job.details }}</p>
</template>

<script>
export default {
  props: ["id"],
  data() {
    return {
      job: null,
    };
  },
  mounted() {
    fetch("http://localhost:3000/jobs/" + this.id)
      .then((res) => res.json())
      .then((data) => (this.job = data))
      .catch((err) => console.log(err.message));
  },
};
</script>

<style>
</style>