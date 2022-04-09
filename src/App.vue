<template>
  <div id="app">
    <router-link to="/">HomePage</router-link>
    <br>
    <router-link to="/about">AboutPage</router-link>
    <router-view/>
  </div>
</template>

<style>


#app {
  display: inline-block;
  width: 100%;
  
}
</style>
