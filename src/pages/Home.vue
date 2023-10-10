<template>
  <div>
    <div>
      <Header />
    </div>
    <div
      class="container grid grid-cols-2 px-1 pt-2 sx:gap-5 sm:gap-10"
    >
      <Education />
      <Language />
      <Projects />
      <Skills />
    </div>
  </div>
</template>
<script setup>
import Header from "../components/header/Header.vue";
import Language from "../components/section/Language.vue";
import Education from "../components/section/Education.vue";
import Projects from "../components/section/Projects.vue";
import Skills from "../components/section/Skills.vue";
</script>
<style></style>
