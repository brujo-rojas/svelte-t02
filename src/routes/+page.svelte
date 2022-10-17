<layout>
	<h1>Welcome to your library project</h1>
	<p>Create your package using @sveltejs/package and preview/showcase your work with SvelteKit</p>
	<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

	<div class="box">
		<div class="mini-box" />
		<div class="mini-box" />
		<div class="mini-box" />
		<div class="mini-box" />
	</div>

	<a href="/login">To Login</a>
</layout>

<style lang="scss">
	.box {
		width: 300px;
		height: 300px;
		background-color: red;
		.mini-box {
			width: 50px;
			height: 50px;
			margin: 1em;
			background-color: blue;
		}
	}
</style>
