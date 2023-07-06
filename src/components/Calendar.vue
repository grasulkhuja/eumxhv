<template>
  <Calendar />
  <DatePicker v-model="date">
</template>

<script>
import { ref } from 'vue'

const date = ref(new Date())

</script>
