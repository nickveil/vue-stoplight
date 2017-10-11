<template>
	<div class="light">
		<bulb light-color="red" 
				v-on:bulbClicked="catchbulbClicked"/>
		<bulb light-color="yellow" 
				v-on:bulbClicked="catchbulbClicked"/>
		<bulb light-color="green" 	
				v-on:bulbClicked="catchbulbClicked"/>
	</div>
</template>

<script>
	import bulb from './bulb.vue';
	export default {
		name : 'light',
		components : {
			bulb
		},
		methods: {
			catchbulbClicked : function(color){
				this.$emit('lightClicked',color);
			}
		}
	}
</script>

<style>
	.light {
		width : 66px;
		display: block;
		border: 2px solid #000;
		background-color: #999;
		margin: auto; 
	}
</style>