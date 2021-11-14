<script>
    export let variant = '';
    export let onClick = () => {};

    $: classButton = `btn-${variant}`;
</script>

<button class={'btn ' + classButton} on:click={onClick}>
    <slot />
</button>

<style>
    .btn {
        border: none;
        padding: 10px 29px;
        margin: 0;
        font-weight: 600;
        color: #5a5a5a;
        border-radius: 8px;
    }

    .btn-primary {
        color: white;
        background-color: #5151f5;
    }
</style>
