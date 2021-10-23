<template>
    <table
        class="
          table
          text-gray-400
          border-separate
          space-y-6
          text-sm
          w-full
         
        "
      >
        <thead class="bg-gray-800 text-gray-500">
          <tr>
            <th class="p-3">Nome</th>
            <th class="p-3 text-left">Email</th>
            <th class="p-3 text-left">CPF</th>
            <th class="p-3 text-left">Idade</th>
            <th class="p-3 text-left">Ações</th>
          </tr>
        </thead>
        <tbody>
          <tr
            class="bg-gray-800"
            v-for="cliente in clientes"
            :key="cliente.cpf"
          >
            <td class="p-3">{{ cliente.nome }}</td>
            <td class="p-3">{{ cliente.email }}</td>
            <td class="p-3">{{ cliente.cpf }}</td>
            <td class="p-3">{{ cliente.idade }}</td>
            <td class="p-3">
              <a href="#" class="text-gray-400 hover:text-gray-100 mx-2">
                <i class="material-icons-outlined text-base">edit</i>
              </a>
              <a href="#" class="text-gray-400 hover:text-gray-100 ml-2">
                <i class="material-icons-round text-base">delete_outline</i>
              </a>
            </td>
          </tr>
        </tbody>
      </table>
</template>
<style scoped>
.table {
  border-spacing: 0 15px;
}

i {
  font-size: 1rem !important;
}

.table tr {
  border-radius: 4px;
}

tr td:nth-child(n + 5),
tr th:nth-child(n + 5) {
  border-radius: 0 4px 4px 0;
}

tr td:nth-child(1),
tr th:nth-child(1) {
  border-radius: 4px 0 0 4px;
}
</style>
<script>
export default {
    props:["clientes"]
}
</script>