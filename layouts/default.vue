<template>
  <div class="container">
    <div class="logo-bg"></div>
    <div class="logo"></div>
    <nav>
      <ul>
        <li>home</li>
        <li>about</li>
        <li>events</li>
        <li>support</li>
        <li>contact</li>
      </ul>
    </nav>
    <nuxt/>
  </div>
</template>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  overflow: hidden;
}

::selection {
  background-color: #315431;
  color: white;
}

::-moz-selection {
  background-color: #315431;
  color: white;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.container {
  height: 100vh;
  width: 100vw;
  background-image: url(/bg.jpg);
  background-size: cover;
  background-position: center;
}

.logo-bg {
  height: 15rem;
  width: 15rem;
  clip-path: polygon(100% 0, 0 0, 0 100%);
  position: absolute;
  left: 0;
  top: 0;
  background-color: rgba(0, 0, 0, 0.6);
}

.logo {
  background-image: url(/logo.png);
  background-size: cover;
  background-position: center;
  position: absolute;
  left: 1rem;
  top: 0rem;
  height: 8rem;
  width: 8rem;
}

nav {
  position: absolute;
  left: 50%;
  top: 2rem;
  transform: translateX(-50%);
  width: 50vw;
}

nav ul {
  display: flex;
  justify-content: space-between;
}

nav ul li {
  font-family: Staatliches, cursive;
  font-size: 1.5rem;
  color: white;
  text-transform: uppercase;
  list-style: none;
  transition: all 0.2s;
  letter-spacing: 0.1rem;
}

nav ul li:hover {
  cursor: pointer;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid white;
}
</style>
