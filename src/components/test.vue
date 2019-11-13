<template>
	<div>
		<!-- Mostrar variable -->
	<h1>{{title}}</h1>
		<!-- Mostrar con directrices -->
	<div v-text="title"></div>
		<!-- if -->
	<div v-if="showName">
		<p>{{user.firstName}}</p>
	</div>
	<div v-else>
		<p>No se puede mostrar nombre</p>
	</div>
	<hr/>
		<!-- Mostrar listado -->
	<ul>
		<li v-for="task in tasks">
			{{task.title}}
		</li>
	</ul>
</div>
</template>

<script>
	
	export default{
		data(){
			return{
			title: 'Hola Mundo',
			user: {
				firstName: 'Asier',
				lastName: 'García'
			},
			myHtml: '<h3>Test html</h3>',
			showName: false,
			tasks: [
				{title: 'eat'},
				{title: 'dinner'}				
			]
		}
	}
}
	

</script>

<style>
	

</style>