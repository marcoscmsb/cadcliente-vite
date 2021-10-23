<template>
  <link
    href="https://fonts.googleapis.com/css?family=Material+Icons|Material+Icons+Outlined|Material+Icons+Two+Tone|Material+Icons+Round|Material+Icons+Sharp"
    rel="stylesheet"
  />
  <div class="h-full bg-gray-900">
    <h1 class="text-white text-4xl text-center pt-20 mb-10">{{ titulo }}</h1>
    <div class="grid grid-cols-12 gap-4">
      <app-cliente-form @adicionar="adicionarCliente" :cliente="cliente" />
    </div>
    <div class="overflow-auto lg:overflow-visible grid grid-cols-12 gap-4">
      <div
        class="
          col-span-10 col-start-2
          sm:col-span-8 sm:col-start-3
          md:col-span-6 md:col-start-4
        "
      >
        <app-cliente-table :clientes="clientes" />
      </div>
    </div>
  </div>
</template>

<script>
import AppClienteForm from "./components/AppClienteForm.vue";
import AppClienteTable from "./components/AppClienteTable.vue";
export default {
  components: {
    AppClienteTable,
    AppClienteForm,
  },
  data() {
    return {
      titulo: "Cadcliente",
      cliente: {},
      clientes: [],
    };
  },
  methods: {
    adicionarCliente(novoCliente) {
      this.clientes.push(novoCliente);
    },
  },
};
</script>
