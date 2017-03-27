<template lang="pug">
.hello
  .header.u-full-width.shadow.raised
    .brand-title.u-pull-left Markadillo
  .sidebar.fixed.u-pull-left
    template(v-for="i in 9")
      button Button {{i}}
  .window
    .tab-bar.u-pull-left.u-full-width
      .tab.u-pull-left.active.h5 View
      .tab.u-pull-left.h5 Edit
    .container
      h1 Page Title
      div Page content goes here

</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/markss';

.header {
  background-color: $primary-color;
  color: $secondary-color;
  height: 10rem;
  top: 0px;

  .brand-title {
    font-family: 'Aero Matics';
    font-size: 6rem;
    font-variant: small-caps;
  }
}

.sidebar {
  background-color: $light-grey;
  font-family: 'Aero Matics';

  button {
    background-color: $primary-color;
    letter-spacing: .2rem;

    &.sidebar-toggle {
      position: absolute;
      bottom: 12rem;
    }
  }
}

.window {
  margin-top: 10rem;
  margin-left: 18rem;

  h1, .h1,
  h2, .h2,
  h3, .h3 {
    font-family: 'Aero Matics';
  }

  h1, .h1 {
    font-variant: small-caps;
  }

  .tab {
    font-family: 'Aero Matics';
    letter-spacing: .1rem;
  }
}

a {
  color: $link-color;

}
</style>
