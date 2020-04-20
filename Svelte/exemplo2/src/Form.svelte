<script>
    export let handleSubmit = function(event) {
        // valor padrão da prop
    };
</script>

<form on:submit|preventDefault={handleSubmit}>
    <label for = "search"> Pesquisa: </label>
    <input type = "search" id = "search" obrigatorio />
    <button type = "submit"> Pesquisar </button>
</form>