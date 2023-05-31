<template>
  <div class="card flex justify-content-center">
    <Dropdown
      v-model="selectedCity"
      editable
      :options="cities"
      optionLabel="name"
      placeholder="Select a City"
      class="w-full md:w-14rem"
      itemValue="name"
    />
  </div>
  <div class="card flex justify-content-center">
    <VCustomSelect
      v-model="selectedCity"
      :options="cities"
      label="name"
      placeholder="Select a City"
      class="w-full md:w-14rem"
    />
  </div>
  <div class="card flex justify-content-center">
    <va-select
      v-model="selectedCity"
      class="mb-6"
      label="track by"
      :options="cities"
      track-by="name"
      text-by="name"
    />
  </div>

  <div class="card flex justify-content-center">{{ selectedCity }}</div>
</template>

<script setup>
import { ref } from 'vue';

const selectedCity = ref({ name: 'Rome', code: 'RM' });
const cities = ref([
  { name: 'New York', code: 'NY', id: 1 },
  { name: 'Rome', code: 'RM', id: 2 },
  { name: 'London', code: 'LDN', id: 3 },
  { name: 'Istanbul', code: 'IST', id: 4 },
  { name: 'Paris', code: 'PRS', id: 5 },
]);
</script>
