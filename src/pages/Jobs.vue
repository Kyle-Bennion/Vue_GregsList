
<template>
  <div>
    <job v-for="j in jobs" :key="j.id" :jobprop="j" />
  </div>
</template>

<script>
import job from "../components/Job";
export default {
  mounted() {
    this.$store.dispatch("getAllJobs");
  },
  computed: {
    jobs() {
      return this.$store.state.jobs;
    },
  },
  components: {
    job,
  },
};
</script>

<style>
</style>