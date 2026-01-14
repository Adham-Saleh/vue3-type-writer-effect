<script setup>
import { ref } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import TypeWriterEffect from "../../src/components/TypeWriterEffect.vue";

const btnDisabled = ref(true);
</script>

<template>
  <div style="max-width: 500px">
    <h1>TypeWriterEffect</h1>
    <TypeWriterEffect
      text="Welcome to TypeWriterEffect, enjoy animating your text. Now with the ability to know when did your animated text ended."
      typeSpeed="normal"
      textColor="white"
      fontSize="20px"
      cursorColor="white"
      @typeEnded="btnDisabled = false"
    />

    <a
      href="https://github.com/reusable-ui-tr/vue3-type-writer-effect/tree/main"
      target="_blank"
    >
      <button :disabled="btnDisabled">GitHub</button>
    </a>
    <a
      href="https://www.npmjs.com/package/@reusable-ui-tr/vue3-type-writer-effect?activeTab=readme"
      target="_blank"
    >
      <button :disabled="btnDisabled">Docs</button>
    </a>
  </div>
</template>

<style scoped>
button {
  margin: 0 6px;
}

button:disabled {
  cursor: not-allowed;
}
</style>
