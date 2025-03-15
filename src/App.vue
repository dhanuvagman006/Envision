<script>
import { ref } from "vue";

export default {
  setup() {
    const name = ref("Dhanush");
    const college = ref("Srinivas Institute of Technology");
    const identifier = ref("nigiga");
    const nigganame="Nikshith";
    const text="";

    return { name, college, identifier,nigganame,text};
  }
};
</script>

<template>
  <h1>{{ name }}</h1>
  <br />
  <h2>{{ college }}</h2>
  <div v-if="identifier === 'Maniga'">
    <br>
    <h1>{{ nigganame}} is Nigga,alwa magaa?</h1>
  </div>
</template>
