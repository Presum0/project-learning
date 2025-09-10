<script>
  let dollars = $state(0)
  let cents = $state(0)
  
  $effect(() => {
    if (dollars > 0) {
      cents = dollars * 100;
    }
  })
</script>

<main class="min-h-screen flex flex-col items-center justify-center p-4 bg-gray-900 text-white">
  <label for="dollars">Dollars</label>
    <input 
    type="number" 
    id="dollars"
    bind:value={dollars}
    class="w-32 p-2 bg-gray-800 text-white rounded border border-gray-600 focus:outline-none focus:border-blue-500 [appearance:textfield] [&::-webkit-outer-spin-button]:appearance-none [&::-webkit-inner-spin-button]:appearance-none"
  >
  <br>
  <label for="cents">Cents</label>
    <input 
    type="number" 
    id="cents"
    bind:value={cents}
    class="w-32 p-2 bg-gray-800 text-white rounded border border-gray-600 focus:outline-none focus:border-blue-500 [appearance:textfield] [&::-webkit-outer-spin-button]:appearance-none [&::-webkit-inner-spin-button]:appearance-none"
  >

</main>
