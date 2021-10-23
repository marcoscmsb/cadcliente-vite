<template>
  <form
    class="
      w-full
      bg-gray-800
      rounded-lg
      sahdow-lg
      p-12
      justify-center
      items-center
      col-span-10 col-start-2
      sm:col-span-8 sm:col-start-3
      md:col-span-6 md:col-start-4
      grid grid-cols-1
      lg:grid-cols-2
      gap-2
    "
  >
    <input
      class="
        bg-transparent
        outline-none
        border-gray-700 border-2
        px-5
        py-2
        rounded
        focus:border-blue-500
        ease-in
        duration-200
        transition
        text-white
      "
      v-model="cliente.nome"
      type="text"
      placeholder="Nome Completo"
    />

    <input
      class="
        bg-transparent
        outline-none
        border-gray-700 border-2
        px-5
        py-2
        rounded
        focus:border-blue-500
        ease-in
        duration-200
        transition
        text-white
      "
      v-model="cliente.email"
      type="email"
      placeholder="Email"
    />
    <input
      class="
        bg-transparent
        outline-none
        border-gray-700 border-2
        px-5
        py-2
        rounded
        focus:border-blue-500
        ease-in
        duration-200
        transition
        text-white
      "
      v-model="cliente.cpf"
      type="text"
      placeholder="CPF"
    />
    <input
      class="
        bg-transparent
        outline-none
        border-gray-700 border-2
        px-5
        py-2
        rounded
        focus:border-blue-500
        ease-in
        duration-200
        transition
        text-white
      "
      v-model="cliente.idade"
      type="number"
      placeholder="Idade"
    />
    <button
      class="
        px-5
        py-2
        uppercase
        rounded
        border-gray-700 border-2
        text-white
        hover:bg-blue-500 hover:border-blue-500
        ease-in
        duration-200
        transition
        col-span-full
      "
      @click="adicionar"
      type="button"
    >
      Adicionar
    </button>
  </form>
</template>
<script>
export default {
    props:["cliente"],
     methods: {
    adicionar() {
      this.$emit("adicionar",Object.assign({}, this.cliente)) //Deep Copy
      //this.clientes.push(Object.assign({}, this.cliente));
    },
  },
}
</script>
