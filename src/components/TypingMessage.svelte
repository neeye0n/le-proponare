<script>
    import { onMount } from 'svelte';

    let message = '';
    const text = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.";

    onMount(() => {
        // Simulate typing effect
        let index = 0;
        const interval = setInterval(() => {
            message = text.slice(0, index);
            index++;
            if (index > text.length) {
                clearInterval(interval);
            }
        }, 120); // Adjust speed of typing (milliseconds)
    });
</script>

<style>
    p {
        font-size: 19px;
        white-space: pre-wrap; /* Preserve line breaks */
        line-height: 1.6;
        text-indent: 2em;
        text-align: justify;
        width: 80%;
        margin: 0 auto;
    }
</style>

<p>{message}</p>
