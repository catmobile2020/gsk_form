<template>
  <div class="title">Welcome to Does Tracker</div>

  <v-card class="mx-auto my-3" max-width="500">
    <div class="container">
      <v-select
        v-model="selectedProduct"
        variant="outlined"
        :items="items"
        label="Select Product"
      ></v-select>
      <v-select
        v-model="selectedDose"
        variant="outlined"
        :items="dose"
        label="Select Dose"
      ></v-select>
      <v-text-field
        v-model="selectedDateTime"
        variant="outlined"
        type="date"
        label="Date"
      ></v-text-field>
      <v-col cols="12" md="12" class="d-flex justify-center">
        <add-to-calendar-button
          styleLight="--btn-background: #F1541A; --btn-text: #fff; "
          styleDark="--btn-background: #000;"
          width="100%"
          name="Title"
          options="'Apple','Google'"
          location="World Wide Web"
          endDate="2024-01-11"
          startTime="10:15"
          endTime="23:30"
          startDate="2024-01-11"
          timeZone="Asia/Riyadh"
        ></add-to-calendar-button>
      </v-col>
    </div>
  </v-card>
</template>

<script>
import "add-to-calendar-button";

export default {
  name: "HelloWorld",
  data: () => ({
    items: [
      "Seretide",
      "Seretide",
      "Seretide",
      "Seretide",
      "Seretide",
      "Seretide",
      "Seretide",
      "Seretide",
      "Seretide",
    ],
    dose: ["Once Daily", "Twice Daily", "Every Week", "Every Month"],
    menu: false,
    date: new Date().toISOString().substr(0, 10), // set initial date to today
    selectedProduct: null,
    selectedDose: null,
    selectedDateTime: new Date().toISOString().substr(0, 10),
  }),
  props: {
    msg: String,
  },
  computed: {
    formattedStartDate() {
      const date = new Date(this.selectedDateTime);
      const formattedDate = date.toISOString().split("T")[0];
      return formattedDate;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.container {
  padding: 30px;
}
.title {
  font-size: 22px;
  font-weight: 700;
  color: #5e6366;
}
</style>
