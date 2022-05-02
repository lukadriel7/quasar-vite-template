<template>
  <q-page class="row items-center justify-evenly">
    {{ hello }}
    <q-btn label="Click me" @click="notify(`${level}`)"></q-btn>
    <!-- <use-mouse v-slot="{ x, y }"> x: {{ x }}, y: {{ y }} </use-mouse> -->
  </q-page>
</template>

<script setup lang="ts">
const hello = ref('hello');
const { notify } = useQuasar();
const { level } = useBattery();
</script>
