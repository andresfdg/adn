<template>
  <div class="container mt-3">
    <h1>Hello!</h1>

    <Adn />
  </div>
</template>

<script>
import Adn from "@/components/Adn.vue";
export default { components: { Adn } };
</script>

<style scoped>
.container {
  text-align: center;
  font-family: "Roboto Condensed", sans-serif;
  font-size: 25px;
}
</style>
