<template>
  <div class="card text-center m-3">
    <h5 class="card-header">Simple GET Request</h5>
    <v-responsive
    class="mx-auto"
    max-width="344"
  >
  <input
  :value="text"
  @input="event => text = event.target.value">
  </v-responsive>
    <button @click="makeRequest">Make Get request</button>
    <div class="card-body">Result: {{ totalVuePackages }}</div>

  </div>
</template>
  
<script>
export default {
  name: "get-request",
  data() {
    return {
      totalVuePackages: null
    };
  },
  methods: { //"https://randomuser.me/api/"
    makeRequest() {
      fetch(this.text)
        .then(response => response.json())
        .then(data => (this.totalVuePackages = data));
    }
  },
  created() {
    // Simple GET request using fetch
    //fetch("https://randomuser.me/api/")
    //  .then(response => response.json())
    //  .then(data => (this.totalVuePackages = data.results));
  }
};
</script>
  