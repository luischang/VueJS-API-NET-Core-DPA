<template>
  <v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">First Name</th>
          <th class="text-left">Last Name</th>
          <th class="text-left">City</th>
          <th class="text-left">Country</th>
          <th class="text-left">Phone</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in clientes" :key="item.id">
          <td>{{ item.firstName }}</td>
          <td>{{ item.lastName }}</td>
          <td>{{ item.city }}</td>
          <td>{{ item.country }}</td>
          <td>{{ item.phone }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      clientes: [],
      desserts: [
        {
          name: "Frozen Yogurt",
          calories: 159,
        },
        {
          name: "Ice cream sandwich",
          calories: 237,
        },
        {
          name: "Eclair",
          calories: 262,
        },
        {
          name: "Cupcake",
          calories: 305,
        },
        {
          name: "Gingerbread",
          calories: 356,
        },
        {
          name: "Jelly bean",
          calories: 375,
        },
        {
          name: "Lollipop",
          calories: 392,
        },
        {
          name: "Honeycomb",
          calories: 408,
        },
        {
          name: "Donut",
          calories: 452,
        },
        {
          name: "KitKat",
          calories: 518,
        },
      ],
    };
  },
  methods: {
    loadCustomers() {
      let url = "http://localhost:63292/api/Customer/GetCustomer";

      axios.get(url, {}).then((response) => {
        console.log(response);
        this.clientes = response.data;
      });
    },
  },
  created() {
    this.loadCustomers();
  },
};
</script>