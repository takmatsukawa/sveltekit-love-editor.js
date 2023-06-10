<script>
    import {onMount} from 'svelte';

    let div;

    onMount(async () => {
        const EditorJS = await import('@editorjs/editorjs');
        const Header = await import('@editorjs/header');
        const List = await import('@editorjs/list');
        const editor = new EditorJS.default({
            holder: div,
            tools: {
                header: Header.default,
                list: List.default
            }
        });
    });
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<div bind:this={div} />