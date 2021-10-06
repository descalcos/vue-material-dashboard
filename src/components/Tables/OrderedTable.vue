<template>
  <div>
    <md-table v-model="users" :table-header-color="tableHeaderColor">
      <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="ID">{{ item.id }}</md-table-cell>
        <md-table-cell md-label="Local">{{ item.name }}</md-table-cell>
        <md-table-cell md-label="Dia">{{ item.salary }}</md-table-cell>
        <md-table-cell md-label="Carro">{{ item.country }}</md-table-cell>
        <md-table-cell md-label="Tempo">{{ item.city }}</md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "ordered-table",
  props: {
    tableHeaderColor: {
      type: String,
      default: ""
    }
  },
  data() {
    return {
      selected: [],
      users: [
        {
          id: 1,
          name: "Ford SP",
          salary: "05/02/2020",
          country: "Elétrica",
          city: "3 horas"
        },
        {
          id: 2,
          name: "Ford SBC",
          salary: "15/12/2020",
          country: "Revisão",
          city: "1 dia"
        },
        {
          id: 3,
          name: "Ford SP",
          salary: "09/04/2021",
          country: "Motor",
          city: "5 horas"
        },
        {
          id: 4,
          name: "Ford SP",
          salary: "20/11/2021",
          country: "Revisão",
          city: "1 dia"
        }
      ]
    };
  }
};
</script>
