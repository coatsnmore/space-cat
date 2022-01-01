<script>
	import { page } from "$app/stores";
	// import logo from "./svelte-logo.svg";
	let logo = "space-cat-logo.png";
</script>

<header>
	<!-- <div class="corner">
		<a href="https://kit.svelte.dev">
			<img src="space-cat-logo.png" alt="Space Cat" />
		</a>
	</div> -->

	<nav>
		<div id="space-cat-nav">
			<img src="space-cat-logo.png" alt="Space Cat" />

			<ul>
				<li class:active={$page.url.pathname === "/"}>
					<a sveltekit:prefetch href="/">Home</a>
				</li>
				<li class:active={$page.url.pathname === "/about"}>
					<a sveltekit:prefetch href="/about">About</a>
				</li>
				<!-- <li class:active={$page.url.pathname === "/blog"}>
					<a sveltekit:prefetch href="/blog">Blog</a>
				</li> -->
			</ul>
		</div>
	</nav>

	<div class="corner">
		<!-- TODO put something else here? github link? -->
	</div>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
	}

	.corner {
		width: 3em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li.active::before {
		--size: 6px;
		content: "";
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--accent-color);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--heading-color);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--accent-color);
	}

	nav img {
		width: 10%;
	}

	#space-cat-nav {
		display: flex;
		align-items: center;
		justify-content: center;
		background-color: white;
		flex-direction: column;
		width: 100%;
	}
</style>
