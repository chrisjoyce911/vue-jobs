<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h2>{{ job.title }}</h2>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {
          title: "UX Designer",
          id: 1,
          details:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima ad incidunt, officiis repellat asperiores, dolorem voluptatibus quibusdam ea sint ex unde explicabo amet recusandae!",
        },
        {
          title: "Web Developer",
          id: 2,
          details:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptatum id aliquid laboriosam praesentium, nobis sit adipisci impedit nisi aliquam recusandae reprehenderit dolorum minus, mollitia",
        },
        {
          title: "Vue Developer",
          id: 3,
          details: "Lorem ipsum dolor sit amet consectetur, adipisicing elit.",
        },
      ],
    };
  },
};
</script>

<style>
.job h2 {
  background: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
.job h2:hover {
  background: #ddd;
}
.job a {
  text-decoration: none;
}
</style>
