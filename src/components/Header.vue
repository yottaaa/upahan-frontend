<template>
    <nav class="navbar" role="navigation" aria-label="main navigation">
        <div class="navbar-brand">
            <a class="navbar-item" href="https://bulma.io">
            <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
            </a>

            <a 
                role="button" class="navbar-burger" 
                v-bind:class="{'is-active': toggle}"
                aria-label="menu" aria-expanded="false" 
                data-target="navbarBasicExample"
                v-on:click="toggle = !toggle"
            >
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
            </a>
        </div>

        <div 
            id="navbarBasicExample" class="navbar-menu"
            v-bind:class="{'is-active': toggle}"
        >
            <div class="navbar-start">
                <router-link class="navbar-item" to="/">Home</router-link>
                <router-link class="navbar-item" to="/about">About</router-link>

            <div class="navbar-item has-dropdown is-hoverable">
                <a class="navbar-link">
                More
                </a>

                <div class="navbar-dropdown">
                <a class="navbar-item">
                    About
                </a>
                <a class="navbar-item">
                    Jobs
                </a>
                <a class="navbar-item">
                    Contact
                </a>
                <hr class="navbar-divider">
                <a class="navbar-item">
                    Report an issue
                </a>
                </div>
            </div>
            </div>

            <div class="navbar-end">
            <div class="navbar-item">
                <div class="buttons">
                <a class="button is-primary">
                    <strong>Sign up</strong>
                </a>
                <a class="button is-light">
                    Log in
                </a>
                </div>
            </div>
            </div>
        </div>
        </nav>
</template>

<script>
export default {
  name: 'Header',
  data: function() {
      return {
          toggle: false
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
