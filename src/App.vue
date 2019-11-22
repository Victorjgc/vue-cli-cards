<template>
  <div id="app">
    <BaseCard nickname="scar"></BaseCard>
    <BaseCard nickname="wolf"></BaseCard>
    <button class="btn" @click="showCard">Press</button>
    <!--BaseCard v-for="u in chars" :key="u">
      {{ u.chars }}
    </BaseCard-->
  </div>
</template>

<script>
import BaseCard from "@/components/BaseCard.vue";
export default {
  name: "app",
  components: {
    BaseCard
  },
  methods: {
    showCard() {
      alert("You!");
    }
  }
};
</script>

<style>
body {
  background: #4187b5;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  border: 1px solid blue;
  display: flex;
  justify-content: center;
}
.btn {
  width: 100px;
  height: 50px;
}
</style>
