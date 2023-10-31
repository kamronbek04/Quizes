<template>
  <div class="result">
    <p>Your Result is ...</p>
    <h1>{{ numberOfCorrectAnswers }}/{{ quizQuestionLength }}</h1>
    <RouterLink class="back" to="/">Go back</RouterLink>
  </div>
</template>
<script setup>
import { defineProps } from "vue";
import { RouterLink } from "vue-router";

const { quizQuestionLength, numberOfCorrectAnswers } = defineProps([
  "numberOfCorrectAnswers",
  "quizQuestionLength",
]);
</script>
<style scoped>
.back {
  padding: 10px 20px;
  background-color: red;
  color: white;
  border-radius: 10px;
}
.result {
  text-align: center;
  padding: 100px 0;
}
p {
  font-size: 25px;
}
h1 {
  font-size: 80px;
}
</style>
