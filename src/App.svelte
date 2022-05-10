<script>
  import Card from "./Card.svelte";

  let toggle = false;

function fonction(event) {
  console.log(`chang: ${event.detail.txt}`)
}
function toggleF() {
  toggle = !toggle
}
</script>

<h1>Je suis le parent</h1>
<button on:click={toggleF} >Toggle</button>

{#if toggle}
<Card on:info-carte={fonction}>
  <h2>Mon titre depuis le parent</h2>
  <div slot="contenu">
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum maiores quo ad? Cum eos maxime ipsam repudiandae odit architecto aspernatur, libero, ea quibusdam consequatur sapiente.</p>
  </div>
</Card>
{/if}

<style>
</style>
