<template>
  <message-box>
    Hi! My name is SwasthyaBot and I am here to help you.
  </message-box>
</template>

<script setup>
import { computed, onMounted, watch } from "vue";
import { useFlowStore } from "@/stores/flow.store";

const flow = useFlowStore();

onMounted(async () => {
  await flow.push("InitialInteraction");

  watch(flow.flow, () => {
    setTimeout(() => {
      document.querySelector("#scroll").scrollIntoView();
    }, 200);
  });
});
</script>
