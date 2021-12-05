<script>
	import { page } from '$app/stores';

	console.log($page.params);
</script>

<h1>{$page.params.slug}</h1>
