<template>
  <div class="text-subtitle-1 ml-4">
    {{ date }}
  </div>
</template>

<script>
import { format } from 'date-fns'

export default {
  data() {
    return {
      date: ''
    }
  },
  methods: {
    getDate() {
      this.date = format(new Date(), 'MMMM d yyyy, hh:mm a')
      setTimeout(this.getDate, 60000)
    }
  },
  mounted() {
    this.getDate()
  }
}
</script>

<style>

</style>