<template>
  <div id="app">
    <div id="nav">
      <div id="container-nav">
        <b-navbar type="dark" variant="dark">
          <b-navbar-nav>
            <b-navbar-brand href="#">
              <img id="logo" src="@/assets/logo.png" alt="Kitten">
            </b-navbar-brand>
            <b-nav-item ><router-link to="/">Home</router-link> |</b-nav-item>
            <b-nav-item > <router-link to="/about">About</router-link> |</b-nav-item>
          </b-navbar-nav>
          <b-navbar-nav id="navBar-right" class="ms-auto">
            <b-nav-item ><router-link to="/connection">Connexion</router-link> |</b-nav-item>
            <b-nav-item > <router-link to="/register">Crée un compte</router-link> |</b-nav-item>
          </b-navbar-nav>
        </b-navbar>
      </div>
    </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#logo {
  max-width: 30px;
}

#nav {
  background-color: #212529;
  width: 100%;
}
#container-car {
  max-height: 93.9vh;
    overflow-y: hidden;
  }

#nav a {
  font-weight: bold;
  color: white;
}

#navBar-right {
  /* padding-left: 35%; */
  text-align: center;
  }

#nav a.router-link-exact-active {
  color: #42b983;
}

#container-nav {
  width: 60%;
  margin: auto;
}
</style>
