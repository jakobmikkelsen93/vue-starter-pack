<script setup>
import { ref, onMounted } from 'vue';
// import ProductService from '@/service/ProductService';

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

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
