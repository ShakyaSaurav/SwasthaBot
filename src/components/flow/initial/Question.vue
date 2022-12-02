<template>
  <message-box>Tell me what's bothering you.  (eg: i have severe headache/stomachache etc.)</message-box>
</template>

<script setup>
import { useFlowStore } from "@/stores/flow.store";

const flow = useFlowStore();

flow.show_input = true;
</script>

<style scoped>
.btn-container {
  display: flex;
  gap: 16px;
  margin-top: 16px;
}
</style>
