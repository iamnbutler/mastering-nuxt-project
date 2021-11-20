<template>
  <div>
    <div v-for="home in homes" :key="home.objectID">
      <HomeCard :home="home" />
    </div>
  </div>
</template>

<script>
import homes from "~/data/homes";

export default {
  head() {
    return {
      title: "Homepage",
      meta: [
        {
          name: "description",
          content: "this is a homepage",
          hid: "description",
        },
      ],
    };
  },
  data() {
    return {
      homes: homes.slice(0, 3),
    };
  },
};
</script>