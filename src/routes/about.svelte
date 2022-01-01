<script context="module">
	import { browser, dev } from "$app/env";

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<div class="content">
	<p>
		This is the personal website of Nicholas Coats AKA <strong
			>Space Cat.</strong
		>
	</p>
	<p>
		I am a software developer with an interest in technology, music,
		sustainable agriculture, science fiction, illustration, comedy, fitness,
		and a million other things that send me down countless and endless
		YouTube rabbit holes.
	</p>
	<div>
		<p>Check out my:</p>
		<ul>
			<li>
				<a href="https://space-cat-music.bandcamp.com/releases">Music</a
				>
			</li>
			<li>
				<a href="https://github.com/coatsnmore">Github</a>
			</li>
			<li>
				<a href="https://www.etsy.com/shop/CosmicCatCommodities">Etsy</a
				>
			</li>
		</ul>
	</div>
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>
