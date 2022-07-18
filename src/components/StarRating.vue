<script setup>
import IconStar from "./icons/IconStar.vue";
</script>

<template>
  <div class="rating">
    <div class="stars">
      <IconStar v-for="i in count" :key="i" class="star checked" />
      <IconStar v-for="i in unchecked" :key="i" class="star" />
    </div>
    <div class="review">{{ count }} ({{ review }})</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      unchecked: 5 - this.count,
    };
  },
  props: { count: Number, review: Number },
};
</script>

<style scoped>
.rating {
  display: flex;
  margin-top: 0.25rem;
}
.star {
  height: 10pt;
  width: 10pt;
  margin-right: 0.15rem;
  color: gainsboro;
}
.checked {
  color: rgb(255, 178, 36);
}
.review {
  font-size: 10.5pt;
  margin-left: 0.25rem;
  color: rgb(180, 180, 180);
  font-weight: bolder;
}
.review:hover {
  color: rgb(0, 45, 194);
}
</style>
