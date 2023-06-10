<script lang="ts">
	import { onMount } from 'svelte';

	let div: HTMLDivElement;

	onMount(async () => {
		// @ts-ignore
		const EditorJS = await import('@editorjs/editorjs');
		const {EDITOR_TOOLS} = await import("./EditorTools");

		const editor = new EditorJS.default({
			holder: div,
			tools: EDITOR_TOOLS,
		});
	});
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<div bind:this={div} />
