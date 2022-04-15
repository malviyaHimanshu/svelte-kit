<script context="module">
    /** @type {import('@sveltejs/kit').Load}*/
    export const load = async ({fetch}) => {
        const req = await fetch('/api/temp');
        const data = await req.json();

        return {
            props: {
                hello: data
            }
        }
    }
</script>

<script>
    export let hello;

    console.log(hello)
</script>


<h1>Hello to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
