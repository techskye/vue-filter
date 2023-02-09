<template>
	<h1>Color Picker Game in Composable format</h1>
  
	<div>{{ message }}</div>
  
	<button v-for="color in colors" :key="color" @click="matchColor(color)">
	  {{ color }}
	</button>
  </template>
  
  <script>
  export default {
	name: "ColorPickerGame",
	data() {
	  return {
		  colors: ["green", "red", "blue", "purple"],
		  message: "Pick a color...",
	  };
	},
	methods: {
	  matchColor (value) {
		// do a random color based on the array index;
		const randomNumber = Math.floor(Math.random() * 4); //between 1 - 4
		if (this.colors[randomNumber] === value) {
		  this.message = `You win... [answer: ${this.colors[randomNumber]}]`;
		  return;
		}
		this.message = `You loose [answer: ${this.colors[randomNumber]}]`;
	  }
	}
  };
  </script>
  
  <style scoped></style>