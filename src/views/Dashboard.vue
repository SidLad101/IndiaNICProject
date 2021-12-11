<template>
  <div class="about" style="margin:2%">
        <h1>List of Users</h1>
        <v-data-table
          :headers="headers"
          :items="users"
          :items-per-page="10"
          class="elevation-1"
          height="50vh"
        >
          <template v-slot:item.DOB="{ item }">
              {{ new Date(item.DOB) }}
          </template>
        </v-data-table>
  </div>
</template>
<script>
  export default {
    name: 'Dashboard',
    async mounted(){
        const response = await fetch('https://61b4305baf5ff70017ca2128.mockapi.io/api/indianic_api/users/');
        this.users = await response.json();
    },
    data: () => ({
      headers: [
          {
            text: 'Id',
            value: 'id',
          },
          {
            text: 'Name',
            value: 'Name',
          },
          { text: 'Email', value: 'Email' },
          { text: 'Date of Birth', value: 'DOB' },
        ],
        users: [],
    })
  }
</script>
