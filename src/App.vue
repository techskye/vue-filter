<template>
  <ColorPickerGame v-if="currentLesson === 'color-picker-game'" />
  <!-- <Recap_01_02_2023 v-else /> -->
  <ColorPickerGameComposable />
</template>

<script>
import ColorPickerGameComposable from "./components/ColorPickerGameComposable.vue";
import ColorPickerGame from "./components/ColorPickerGame.vue";
// import Recap_01_02_2023 from "./components/Recap_01_02_2023.vue";
export default {
  components: {
    ColorPickerGame,
    // Recap_01_02_2023,
    ColorPickerGameComposable,
  },
  data() {
    return {
      currentLesson: "color-picker-game",
    };
  },
};
</script>

<style scoped></style>