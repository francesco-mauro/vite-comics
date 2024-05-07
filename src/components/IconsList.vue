<script>
export default{
  data() {
    return {
      images: [
        {
          image: "buy-comics-digital-comics.png",
          title: "DIGITAL COMICS",
        },
        {
          image: "buy-comics-merchandise.png",
          title: "CD MERCHANDISE",
        },
        {
          image: "buy-comics-subscriptions.png",
          title: "SUBSCRIPTION",
        },
        {
          image: "buy-comics-shop-locator.png",
          title: "COMIC SHOP LOCATOR",
        },
        {
          image: "buy-dc-power-visa.svg",
          title: "DC POWER VISA",
        },
      ],
    };
  },
  methods: {
    getImageUrl(imageName){
      return new URL(`../assets/img/${imageName}`, import.meta.url).href
    }


  }
};
</script>

<template>
  <section>
    <div class="container">
      <ul>
        <li v-for="image in images">
          <img :src="getImageUrl(image.image)" alt="">  
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped lang="scss">
@use '../style/partials/_mixins.scss' as *;
@use '../style/partials/variables' as *;

  section{
    background-color: $primary-color;
    padding: 3rem 0;
    color: $white;
  }

</style>
