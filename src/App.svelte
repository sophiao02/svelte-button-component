<svelte:head>
  <link rel="stylesheet" href="https://unpkg.com/tailwindcss@2.2.19/dist/tailwind.min.css"/>
</svelte:head>

<script>
  let isPrimary = true;
  let disabled = false;
</script>

<button
  class="font-bold py-2 px-4 rounded text-white 
         {isPrimary ? 'bg-blue-500 hover:bg-blue-700' : 'bg-gray-500 hover:bg-gray-700'}
         {disabled ? 'opacity-50 cursor-not-allowed' : ''}"
  disabled={disabled}
  on:click={() => isPrimary = !isPrimary}>
  {isPrimary ? 'Primary Button' : 'Secondary Button'}
</button>

<button class="mt-4" on:click={() => disabled = !disabled}>
  {disabled ? 'Enable' : 'Disable'} Button
</button>
