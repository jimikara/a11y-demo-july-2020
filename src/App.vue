<template>
  <div id="app">
    <header id="nav">
      <span class="site-header">😎 Cool Site</span>
      <nav>
        <router-link to="/Login">Not-So-Accessible Login</router-link> |
        <router-link to="/Login-A11y">Accessible Login</router-link>
      </nav>
    </header>
    <div class="page">
      <router-view />
    </div>
  </div>
</template>

<style lang="scss">
@import './styles/variables';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 15px 30px;
  background: $secondary;
  color: $white;
  display: flex;
  justify-content: space-between;

  .site-header {
    font-size: 1.5rem;
    font-weight: 500;
  }

  a {
    font-weight: bold;
    color: #fff;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.page {
  display: flex;
  justify-content: center;
  padding: 60px;
}
</style>
