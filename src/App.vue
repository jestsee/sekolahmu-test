<script setup>
import CardProduct from "./components/CardProduct.vue";
</script>

<template>
  <body>
    <div class="container">
      <CardProduct
        v-for="(item, index) in dummy"
        :key="index"
        :img="item.img"
        :desc="item.desc"
        :title="item.title"
        :source="item.source"
        :rating="item.star"
        :review="item.review"
        :price="item.price"
      />
    </div>
  </body>
</template>

<script>
export default {
  data() {
    return {
      dummy: [
        {
          img: `https://picsum.photos/250?image=${
            Math.floor(Math.random() * 100) + 1
          }`,
          desc: "Living Tech Level Newton (5-8 Tahun)",
          title: "Living Tech Newton (1-Month Free)",
          source: "Sekolah.mu",
          star: Math.floor(Math.random() * 2) + 4,
          review: Math.floor(Math.random() * 98) + 3,
          price: "gratis",
        },
        {
          img: `https://picsum.photos/250?image=${
            Math.floor(Math.random() * 100) + 1
          }`,
          desc: "Living English Level Pioneer (4-5 Tahun)",
          title: "Living English Pioneer (1-Month Free)",
          source: "Sekolah.mu",
          star: Math.floor(Math.random() * 2) + 4,
          review: Math.floor(Math.random() * 98) + 3,
          price: "gratis",
        },
        {
          img: `https://picsum.photos/250?image=${
            Math.floor(Math.random() * 100) + 1
          }`,
          desc: "Living Quran Level Khadijah (4-5 Tahun)",
          title: "Living Quran Khadijah (1-Month Free)",
          source: "Sekolah.mu",
          star: Math.floor(Math.random() * 2) + 4,
          review: Math.floor(Math.random() * 98) + 3,
          price: "gratis",
        },
        {
          img: `https://picsum.photos/250?image=${
            Math.floor(Math.random() * 100) + 1
          }`,
          desc: "Living Math Level Alpha (4-5 Tahun)",
          title: "Living Math Alpha (1-Month Free)",
          source: "Sekolah.mu",
          star: Math.floor(Math.random() * 2) + 4,
          review: Math.floor(Math.random() * 98) + 3,
          price: "gratis",
        },
        {
          img: `https://picsum.photos/250?image=${
            Math.floor(Math.random() * 100) + 1
          }`,
          desc: "Living English Level Finder (6-7 Tahun)",
          title: "Living English Finder (1-Month Free)",
          source: "Sekolah.mu",
          star: Math.floor(Math.random() * 2) + 4,
          review: Math.floor(Math.random() * 98) + 3,
          price: "gratis",
        },
        {
          img: `https://picsum.photos/250?image=${
            Math.floor(Math.random() * 100) + 1
          }`,
          desc: "Living English Level Rover (8-9 Tahun)",
          title: "Living English Rover (1-Month Free)",
          source: "Sekolah.mu",
          star: Math.floor(Math.random() * 2) + 4,
          review: Math.floor(Math.random() * 98) + 3,
          price: "gratis",
        },
        {
          img: `https://picsum.photos/250?image=${
            Math.floor(Math.random() * 100) + 1
          }`,
          desc: "Living Math Level Gamma (6-7 Tahun)",
          title: "Living Math Gamma (1-Month Free)",
          source: "Sekolah.mu",
          star: Math.floor(Math.random() * 2) + 4,
          review: Math.floor(Math.random() * 98) + 3,
          price: "gratis",
        },
        {
          img: `https://picsum.photos/250?image=${
            Math.floor(Math.random() * 100) + 1
          }`,
          desc: "Living Quran Level Ali (6-7 Tahun)",
          title: "Living Quran Ali (1-Month Free)",
          source: "Sekolah.mu",
          star: Math.floor(Math.random() * 2) + 4,
          review: Math.floor(Math.random() * 98) + 3,
          price: "gratis",
        },
        {
          img: `https://picsum.photos/250?image=${
            Math.floor(Math.random() * 100) + 1
          }`,
          desc: "Living Tech Level Einstein (8-10 Tahun)",
          title: "Living Tech Einstein (1-Month Free)",
          source: "Sekolah.mu",
          star: Math.floor(Math.random() * 2) + 4,
          review: Math.floor(Math.random() * 98) + 3,
          price: "gratis",
        },
        {
          img: `https://picsum.photos/250?image=${
            Math.floor(Math.random() * 100) + 1
          }`,
          desc: "Living Tech Level Hawking (10-12 Tahun)",
          title: "Living Tech Hawking (1-Month Free)",
          source: "Sekolah.mu",
          star: Math.floor(Math.random() * 2) + 4,
          review: Math.floor(Math.random() * 98) + 3,
          price: "gratis",
        },
      ],
    };
  },
};
</script>

<style scoped>
body {
  margin: 1.25rem 1rem;
  font-family: Arial, Helvetica, sans-serif;
}
.container {
  display: grid;
  grid-template-columns: repeat(1, minmax(0, 1fr));
  gap: 3rem 2rem;
}
@media only screen and (min-width: 560px) {
  .container {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}
@media only screen and (min-width: 830px) {
  .container {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }
}
@media only screen and (min-width: 1024px) {
  .container {
    grid-template-columns: repeat(4, minmax(0, 1fr));
  }
}
@media only screen and (min-width: 1440px) {
  .container {
    grid-template-columns: repeat(5, minmax(0, 1fr));
    max-width: 1440px;
  }

  body {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
