<template>
  <nav class="vsd-header navbar navbar-expand-lg navbar-light fixed-top py-3">
    <div class="container">
      <router-link to="/" class="navbar-brand">{{ title }}</router-link>
      <button
        v-on:click="isVisible = !isVisible"
        class="navbar-toggler navbar-toggler-right"
        type="button"
        data-toggle="collapse"
        data-target="#navbarResponsive"
        aria-controls="navbarResponsive"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div 
        v-bind:class="{ show: isVisible }"
        class="collapse navbar-collapse" 
        id="navbarResponsive"
      >
        <ul class="navbar-nav ml-auto my-2 my-lg-0">
          <li class="nav-item">
            <router-link :to="{ name: 'about' }" class="nav-link"
              >About</router-link
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "VueSD"
    }
  },
  data: () => ({
      isVisible: false
    })
};
</script>

<style>
.vsd-header {
  background: grey;
}
</style>
