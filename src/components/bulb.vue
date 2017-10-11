<template>
	<div 
	class="bulb" 
	v-bind:class="lightColor"
	v-on:click="reportClickToParent(lightColor)"></div>
</template>

<script>
	export default {
		name : 'bulb',
		props : [ 'lightColor' ],
		methods : {
			reportClickToParent : function(colorClicked){
				this.$emit('bulbClicked', colorClicked);
				
			}
		}
	};
</script>

<style>
	.bulb {
		margin : 5px;
		border : 2px solid #000;
		width : 50px;
		height : 50px;
		border-radius : 50%;
		background-color : #ccc;
	}
	.green {
		background-color : #0f0;
	}
	.yellow {
		background-color : #ff0;
	}
	.red {
		background-color : #f00;
	}
</style>
