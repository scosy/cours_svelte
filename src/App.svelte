<script>
  let toggle = false;
  function toggleClass() {
    toggle = !toggle;
  }
</script>

<button on:click={toggleClass} >Toggle le contenu</button>

<div class={toggle ? 'visible' : 'invisible'}>
  <h2>Voici le contenu</h2>
  <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsam porro quae explicabo minima est nisi corrupti fuga tempora repellendus animi.</p>
</div>

<style>
  .visible {
    width: 250px;
    height: auto;
    padding: 10px;
    background-color: lightblue;
    text-align: center;
  }
  .invisible {
    display: none;
  }
</style>