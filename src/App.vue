<script setup>
import { ref, onMounted } from 'vue';
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
  </nav>
  <router-view/>

  <!-- <div>
      <DataTable :value="products" responsiveLayout="scroll">
          <Column field="code" header="Code"></Column>
          <Column field="name" header="Name"></Column>
          <Column field="category" header="Category"></Column>
          <Column field="quantity" header="Quantity"></Column>
      </DataTable>
  </div> -->

</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
