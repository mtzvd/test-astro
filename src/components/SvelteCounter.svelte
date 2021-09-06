<script>
  let count = 0;

  function add() {
    count += 1;
  }

  function subtract() {
    count -= 1;
  }
</script>


<div id="svelte" class="counter buttons has-addons">
  <button class="button" on:click={subtract}>-</button>
  <button class="button " >{ count }</button>
  <button class="button " on:click={add}>+</button>
</div>

