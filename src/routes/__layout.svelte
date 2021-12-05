<!-- 1. Assign current route's path to `key` prop -->
<script context="module">
	export const load = async ({ page }) => ({
		props: {
			key: page.path
		}
	});
</script>

<script>
	import PageTransition from '$lib/components/PageTransition.svelte';
	export let key;
</script>

<nav>
	<a href="/">Home</a>
	<a href="/about">About</a>
</nav>

<div class="layout">
	<!-- 2. Pass `key` prop to the component so it knows when to transition -->
	<PageTransition refresh={key}>
		<slot />
	</PageTransition>
</div>
