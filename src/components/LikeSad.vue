<template>
  <div style="margin: 3%; display: flex; gap: 10px; justify-content: end">
    <button type="button" class="btn btn-secondary" @click="likeClick">
      <i class="bi bi-emoji-smile"></i> Like {{ like }}
    </button>
    <button type="button" class="btn btn-secondary" @click="sadClick">
      <i class="bi bi-emoji-frown"></i> Sad {{ sad }}
    </button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const like = ref(0);
const sad = ref(0);
function likeClick() {
  like.value++;
}
function sadClick() {
  sad.value++;
}
</script>
<script>
export default {
  name: "LikeSad",
};
</script>
