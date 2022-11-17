<script setup>
import { useFlash } from "@/composables/useFlash";
import { ref, watch } from "vue";
import { useStorage } from "@/composables/useStorage";
let { flash } = useFlash();
let food = useStorage("food", "tacos");
</script>

<template>
  <main>
    <p>What is your fav food?</p>
    <input type="text" v-model="food" />
    <p>How old are you></p>
    <input type="text" v-model="age" />
    <!-- <TheWelcome /> -->
    <button @click="flash('Test', 'it works on the home page')">
      Click me
    </button>
  </main>
</template>
