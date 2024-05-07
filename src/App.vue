<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import IconsList from "./components/IconsList.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
    components: {
        AppHeader,
        AppMain,
        IconsList,
        AppFooter
    },
    data () {
        return {};
    },
};

</script>


<!-- html -->
<template>
    <AppHeader />
    <AppMain />
    <IconsList />
    <AppFooter />


</template>

<style lang="scss">
@use './style/partials/_variables.scss' as *;

h1 {
  color: $primary-color;
}

</style>