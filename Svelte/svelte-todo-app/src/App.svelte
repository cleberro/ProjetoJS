<script>
	import Task from "./Tasks/Task.svelte";
	const projectName = "To Do App";
	const src="https://avatars2.githubusercontent.com/u/23617963?s=40&v=4";

</script>

<section class="section">
	<div class="container">
		<figure class="image is-64x64">
			<img src={src} alt="Svelte3"/>
		</figure>
		<h1 class="title">{projectName}</h1>
		<p class="subtitle">
			My first website made with <strong>Svelte!</strong>
		</p>
	</div>
	<Task />
</section>