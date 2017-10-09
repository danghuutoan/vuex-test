<template>
	<div class="container">
		<div class="row text-center">
			<h3>Clicked {{ $store.state.count }} times , counter is {{ evenOrOdd }} </h3>
			<el-button type="success" @click="increment" >+</el-button>
    		<el-button type="danger" @click="decrement" >-</el-button>
    		<el-button @click="incrementIfOdd" >Increment if odd</el-button>
    		<el-button @click="incrementAsync" >Increment async</el-button>
		</div>
	</div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'

export default {
	name: 'HelloWorld',
	computed: mapGetters([
		'evenOrOdd'
	]),
	methods: mapActions([
		'increment',
		'decrement',
		'incrementIfOdd',
		'incrementAsync'
	])
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
	font-weight: normal;
}

ul {
	list-style-type: none;
	padding: 0;
}

li {
	display: inline-block;
	margin: 0 10px;
}

a {
	color: #42b983;
}
</style>
