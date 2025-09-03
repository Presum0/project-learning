<script>
    export let items = [];
</script>

{#each items as item}
    <button 
        on:click={()=> handleClick(item)}
        class="m-1 p-2 w-10 h-10 flex items-center justify-center bg-gray-700 hover:bg-gray-600 rounded border-none focus:outline-none focus:ring-2 focus:ring-blue-500"
    >
        {item}
    </button>
{/each}