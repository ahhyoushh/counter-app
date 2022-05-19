<script>
    let isLoaded = false;

    const PageLoaded = () => {
        isLoaded = true;
    }
</script>
{#if !isLoaded}
    <div class="Loader" use:PageLoaded>
        <p>Loading..</p>
    </div>
{/if}
<slot />
<style>
    .Loader {
        color: white;
        position: relative;
        display: grid;
        top: 500px;
        justify-items: center;
    }
</style>