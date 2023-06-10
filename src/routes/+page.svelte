<script lang="ts">
	import { onMount } from 'svelte';

	let div: HTMLDivElement;

	onMount(async () => {
		const EditorJS = await import('@editorjs/editorjs');
		const editor = new EditorJS.default({
			holder: div
		});
	});
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<div bind:this={div} />
