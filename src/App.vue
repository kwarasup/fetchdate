<script>
const API_URL = `http://yourname.sit.kmutt.ac.th:8080/api/date`

export default {
  data: () => ({
    date: null
  }),

  created() {
    // fetch on init
    this.fetchData()
  },

  methods: {
    async fetchData() {
      const url = `${API_URL}`
      this.date = await (await fetch(url)).json()
    }
  }
}
</script>

<template>
  <h1>Fetch date from API</h1>

  <p>{{ date }}</p>
</template>
