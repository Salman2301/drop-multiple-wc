
<svelte:options tag="drop-multiple" />


<script>
  let options = [{value:"test" , label: "Test A" , selected: true}] // [{value : "", label: "", selected: true }]
  let showOptions = false;

</script>


<div class="dropdown" on:click={()=>{showOptions = !showOptions}}>
  Select an options
</div>

{#if showOptions}
<div class="options" >
  {#each options as option}
    <div class="option"> {option.label}</div>
  {/each}
</div>
{/if}


<style>
.dropdown {
  width: 250px;
  height: 30px;
  border: 1px solid #ccc;
  border-radius: 3px;
  font-size: 1.2em;
  cursor: pointer;
} 

.option {
  width: 250px;
  border: 1px solid black;
  cursor: pointer;
  
}

</style>