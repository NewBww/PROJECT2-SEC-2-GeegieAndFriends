<script setup>
import { ref } from 'vue'
import SearchIcon from '../atoms/SearchPageButton.vue'

const searchKeyword = ref('')
</script>

<template>
  <div class="h-10 flex rounded-full bg-[#E5E5E5] gap-3 px-3 py-1.5">
    <SearchIcon stroke="black" class="flex-none self-center" />
    <input
      @input="$emit('searchEvent', searchKeyword)"
      v-model="searchKeyword"
      class="bg-transparent flex-1"
      type="text w-full"
      placeholder="What do you want to listen to?"
    />
  </div>
</template>

<style scoped>
input {
  border: 0;
  outline: none;
}
</style>
