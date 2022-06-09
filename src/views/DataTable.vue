<script setup>
import { ref, onMounted } from 'vue';
import ProductService from '..service/ProductService';
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup

onMounted(() => {
            productService.value.getProducts().then(data => products.value = data);
        })

        const products = ref();
        const productService = ref(new ProductService());

</script>

<template>
  <div>
      <DataTable :value="products" responsiveLayout="scroll">
          <Column field="code" header="Code"></Column>
          <Column field="name" header="Name"></Column>
          <Column field="category" header="Category"></Column>
          <Column field="quantity" header="Quantity"></Column>
      </DataTable>
  </div>

</template>