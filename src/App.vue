<template>
  <div id="app">
    <header>
      <nav style="justify-content: center;">
        <div id="nav">
          <ul>
            <li>
              <router-link to="/">Home</router-link>
            </li>
            <li>
              <router-link to="/contact">Contact</router-link>
            </li>
            <li>
              <router-link to="/about">About</router-link>
            </li>
          </ul>
          <br />
          <ul>
            <li>
              <router-link :to="{ name: 'home', hash: '#one' }">Home Anchor 1</router-link>
            </li>
            <li>
              <router-link :to="{ name: 'home', hash: '#two' }">Home Anchor 2</router-link>
            </li>
            <li>
              <router-link :to="{ name: 'contact', hash: '#one' }">Contact Anchor 1</router-link>
            </li>
          </ul>
        </div>
      </nav>
    </header>
    <main>
      <router-view />
    </main>
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

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
