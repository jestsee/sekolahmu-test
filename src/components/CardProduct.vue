<script setup>
import StarRating from "./StarRating.vue";
</script>

<template>
  <div class="card">
    <img :src="img" alt="" />
    <div class="desc">{{ desc }}</div>
    <div class="content">
      <h3 class="title">{{ title }}</h3>
      <div class="source">
        <p>Oleh</p>
        <p class="highlight">{{ source }}</p>
      </div>
      <div class="rating">
        <StarRating :count="rating" :review="review" />
      </div>
      <h3 class="price">{{ price }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    img: String,
    desc: String,
    title: String,
    source: String,
    rating: Number,
    review: Number,
    price: String,
  },
};
</script>

<style scoped>
.card {
  cursor: pointer;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 5px 5px 25px 0.5px rgba(0, 0, 0, 0.15);
}
.card:hover {
  transform: scale(1.1);
}
img {
  width: 100%;
  height: 10rem;
  object-fit: cover;
  display: block;
}
.content {
  padding: 0 0.75rem;
}
.desc {
  font-weight: 800;
  background-color: rgb(255, 178, 36);
  font-size: 8pt;
  padding: 0.5rem 0.75rem;
  margin-top: 0;
  text-align: center;
}
.title {
  margin-top: 0.5rem;
  margin-bottom: 0;
}
.title:hover {
  color: rgb(0, 45, 194);
}
.source {
  align-items: flex-end;
  font-size: 9pt;
  color: gray;
  display: flex;
  margin-top: 0.5rem;
  padding: auto;
}
.source p {
  margin: 0;
  padding: 0;
}
.source:hover {
  color: rgb(0, 45, 194);
}
.source .highlight {
  font-weight: 800;
  margin-left: 0.25rem;
}
.price {
  width: fit-content;
  text-transform: uppercase;
  font-size: 12pt;
  color: rgb(0, 45, 194);
  margin-top: 0.25rem;
  margin-bottom: 1.25rem;
}
.price:hover {
  border-bottom: 1px solid rgb(0, 45, 194);
}
</style>
