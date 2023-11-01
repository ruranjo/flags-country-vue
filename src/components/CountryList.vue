<script setup lang="ts">
import { defineProps } from "vue";
import { ICountry } from "../interfaces/country.interface";
import CountryItem from "./CountryItem.vue";

interface Props {
  countries: ICountry[];
}

defineProps<Props>();
</script>

<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-3">
    <div
      v-for="country in countries"
      class="border border-gray-300 rounded p-3"
    >
      <CountryItem :country="country" />
    </div>
  </div>
</template>