<template>
  <div id="app">
    <ds-page ref="page">
      <template slot="brand">
        <router-link to="/">
          <ds-logo/>
        </router-link>
      </template>
      <navigation slot="sidebar" @navigate="$refs.page.closeDrawer()" />
      <navigation slot="drawer" @navigate="$refs.page.closeDrawer()" />
      <router-view/>
    </ds-page>
  </div>
</template>

<script>
import Navigation from './components/Navigation'

export default {
  name: 'App',
  components: {
    Navigation
  }
}
</script>

<style lang="scss">
</style>
