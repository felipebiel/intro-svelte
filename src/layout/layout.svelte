<script>
    export let title = '';

    import ButtonComponent from '../components/button.svelte';

    let inputValue = '';

    const alertInput = () => {
        alert(inputValue);
    };
</script>

<div class="card">
    <p>{title}</p>
    <input type="text" bind:value={inputValue} />
    <ButtonComponent variant="primary" onClick={alertInput}>Alertar</ButtonComponent>
</div>

<style>
    :global(body) {
        background: #8e2de2; /* fallback for old browsers */
        background: -webkit-linear-gradient(to right, #4a00e0, #8e2de2); /* Chrome 10-25, Safari 5.1-6 */
        background: linear-gradient(
            to right,
            #4a00e0,
            #8e2de2
        ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
        display: flex;
        justify-content: center;
        height: 100vh;
    }

    .card {
        background-color: white;
        height: 220px;
        background-color: white;
        width: 380px;
        padding: 30px 45px;
        align-self: center;
        border-radius: 8px;
        box-shadow: 0px 0px 10px 1px #00000057;
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }

    .card p {
        font-size: 1.5rem;
    }

    .card input {
        padding: 10px;
        margin-bottom: 20px;
    }
</style>
