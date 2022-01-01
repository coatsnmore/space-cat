<script context="module">
	export const prerender = true;
</script>

<script>
	import Counter from "$lib/Counter.svelte";
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section>
	<!-- <h1> -->
	<div class="space-cat">
		<picture>
			<!-- <source srcset="svelte-welcome.webp" type="image/webp" /> -->
			<img src="space-cat.png" alt="Space Cat" />
		</picture>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	.space-cat {
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.space-cat img {
		position: absolute;
		width: 100%;
		/* height: 100%; */
		top: 0;
		display: block;
	}
</style>
