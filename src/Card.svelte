<script>
  import {createEventDispatcher} from 'svelte';
  import {onMount, onDestroy, beforeUpdate, afterUpdate} from 'svelte';

  const dispatch = createEventDispatcher();

  function info() {
    dispatch('info-carte', {txt: 'Panier modifié'})
  }

  onMount(() => {
    console.log('création')
  })
  onDestroy(() => {
    console.log('détruit')
  })
  beforeUpdate(() => {
    console.log('maj')
  })
  afterUpdate(() => {
    console.log('aftermaj')
  })

</script>

<div class="carte">
  <!-- <h2>Je suis le composant enfant</h2> -->
  <slot />
  <slot name="contenu"></slot>
  <button on:click={info} >Clique</button>
</div>

<style>
  .carte {
    border: 1px solid grey;
    padding: 15px;
  }
</style>