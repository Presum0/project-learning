<script>
  import But from "./butt.svelte";
  let a = $state(0);
  let op = $state([1,2,3,4,5,6,7,8,9,0,'+','-','*','/','=']);
  function handleClick(){

  }
</script>

<main class="min-h-screen flex flex-col items-center justify-center p-4 bg-gray-900 text-white">
  <div class="block bg-black w-56 p-4 text-white rounded-xl box-border">
    <input 
      type="text" 
      bind:value={a} 
      class="w-full p-2 rounded bg-gray-800 text-white border border-gray-600 focus:border-blue-500 mb-1 focus:outline-none"
    >
    <div class="grid grid-cols-4 gap-1 mt-2">
      <But items={op} />
    </div> 
    {#each op as i}
      {#if i === '1'}
        {a} = i;
      {/if}
    {/each}
  </div>
</main>
