<template>
  <div class="app-background">
  <AppBar />

    <div class="container app-background">
      <div class="row py-5">
        <BannerT class="my-lg-3" />
        <FutureCommerce class="my-lg-3" />
        <DiscoverPhysical />
        <VirtualItem />
        <GiftShare />
        <SignUp class="mb-5" />
        <br>
        <hr>
        <AppFooter class="py-lg-5 " />
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>

<script>
import AppBar from './components/AppBar.vue'
import BannerT from './components/Banner.vue'
import FutureCommerce from './components/FutureCommerce.vue'
import DiscoverPhysical from './components/DiscoverPhysical.vue'
import VirtualItem from './components/VirtualItem.vue'
import GiftShare from './components/GiftSahre.vue'
import SignUp from './components/SignUp.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',

  components: {
    AppBar,
    BannerT,
    FutureCommerce,
    DiscoverPhysical,
    VirtualItem,
    GiftShare,
    SignUp,
    AppFooter
  },

  data: () => ({
  })
};
</script>