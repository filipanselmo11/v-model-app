<script setup lang="ts">
// import { computed } from 'vue';
// import { useVModel } from '@vueuse/core';
const props = defineProps<{
  placeholder: string,
  // modelValue: {
  //   type: string,
  //   required: true
  // },
}>();

// const emit = defineEmits(['update:modelValue']);

// método 1

// const name = computed({
//   // getter
//   get() {
//     return props.modelValue
//   },
//   // setter
//   set(newValue) {
//     emit('update:modelValue', newValue)
//   }
// });

// Método 2
// const name = useVModel(props, 'modelValue', emit);

// Método 3

const name = defineModel();

</script>

<template>
  <input type="text" v-model="name" :placeholder="props.placeholder">
</template>

