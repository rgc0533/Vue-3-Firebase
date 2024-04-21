<template>
  <div class="backdrop" @click="closeModal">
    <div class="modal-content" :class="{ sale: theme === 'sale' }">
      <h1>{{ header }}</h1>
      <p>{{ text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["header", "text", "theme"],
  methods: {
    closeModal() {
      this.$emit("closemodal");
    },
  },
};
</script>
