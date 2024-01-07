<script lang="ts">
import Tag from "./Tag.vue";

export default {
  props: {
    ingrediente: { type: String, required: true },
  },
  components: { Tag },
  data() {
    return {
      selecionado: true,
    };
  },
};
</script>
<template>
  <button
    class="ingrediente"
    v-on:click="selecionado = !selecionado"
    :aria-pressed="selecionado"
  >
    <Tag :texto="ingrediente" :ativa="selecionado"></Tag>
  </button>
</template>

<style scoped>
.ingrediente {
  cursor: pointer;
}
</style>
