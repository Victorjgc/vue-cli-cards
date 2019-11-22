<template>
  <div class="card" @click="fliped">
    <div class="name">{{ chars[nickname].name }}</div>
    <div class="strong">{{ chars[nickname].strong }}</div>
    <img class="image" :src="chars[nickname].image" alt="" />
    <div class="description">{{ chars[nickname].description }}</div>
  </div>
</template>

<script>
export default {
  name: "BaseCard",
  data() {
    return {
      image: "",
      description: "",
      counter: 0,
      chars: {
        scar: {
          name: "Scar",
          image: require("../assets/scar.jpg"),
          strong: "Strong: 9",
          description: "Just 1 eye to kill"
        },
        wolf: {
          name: "Wolf",
          strong: "Strong 6",
          image: require("../assets/wolf.jpg"),
          description: "I'm the strongest"
        }
      }
    };
  },
  methods: {
    fliped() {
      console.log(this.$el);
      this.$el.classList.toggle("fliped");
    }
  },
  props: {
    nickname: String
  }
};
</script>

<style>
.card {
  background: green;
  margin: 10px;
  align-self: center;

  flex-direction: column;
  border: 1px solid yellow;
  background: white;
}
.image {
  width: 300px;
  height: 450px;
  border: 2px solid black;
  margin: 5px;
  background-position: center;
  background-repeat: no-repeat;
  -webkit-box-shadow: 14px 13px 0px -9px rgba(0, 0, 0, 0.74);
  -moz-box-shadow: 14px 13px 0px -9px rgba(0, 0, 0, 0.74);
  box-shadow: 14px 13px 0px -9px rgba(0, 0, 0, 0.74);
}
.fliped {
  background: red;
}
.fliped * {
  visibility: hidden;
}
</style>
