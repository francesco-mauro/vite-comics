<script>
export default{
  data() {
    return {
      menuItems: [
        {
          title: "Characters",
          active: false,
        },
        {
          title: "Comics",
          active: true,
        },
        {
          title: "Movies",
          active: false,
        },
        {
          title: "Tv",
          active: false,
        },
        {
          title: "Games",
          active: false,
        },
        {
          title: "Collectibles",
          active: false,
        },
        {
          title: "Videos",
          active: false,
        },
        {
          title: "Fans",
          active: false,
        },
        {
          title: "News",
          active: false,
        },
        {
          title: "Shop",
          active: false,
        },
      ],
    };
  },
};
</script>

<template>
  <header>
    <div class="container">
      <img src="../assets/img/dc-logo.png" alt="logo dc">

      <!-- menu -->
      <ul>
        <li v-for="item in menuItems" :class="{ active : item.active}">
          <a href="">{{ item.title }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style scoped lang="scss">
@use '../style/partials/_mixins.scss' as *;
@use '../style/partials/variables' as *;

header .container {
  @include flex(row, space-between, center);

}

ul {
  @include flex(row, space-between, center);
  gap: 1rem;
  list-style-type: none;

  li{

    &.active {
      a {
      text-decoration: none;
      color: $primary-color
    }

    }
    
    a {
      text-decoration: none;
      color: $black
    }

  }


}


</style>
