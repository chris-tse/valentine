<script>
    let open = $state(false)

    function toggleCollapsible() {
        open = !open
    }

</script>

<p class="big top-title">i knew it!</p>
<div class="img-container">
    <img src="/sampo.png" alt="Sampo">
    <img src="/sparkle.png" alt="Sparkle">
</div>

<button on:click={toggleCollapsible} class="collapsible-trigger">View Note (click here)</button>
<div class="collapsible" class:open>
    <p>Write a note to the recipient here!</p>
    <p>Make it as long or as short as you want.</p>
</div>


<style>
  p {
    text-align: center;
  }

  .img-container {
    height: 130px;
  }

  .img-container img {
    width: 130px;
  }

  .collapsible {
    max-height: 0px;
    display: none;
    transition: max-height 0.5s;
    overflow-y: hidden;
    padding: 5px 10px;
    background: #d3d3ff;
    border: 2px solid #b7b7e3;
    border-radius: 5px;
  }

  .collapsible.open {
    max-height: initial;
    display: block;
  }

  .collapsible-trigger {
    margin-top: 10px;
    margin-bottom: 10px;
    padding: 15px;
    color: white;
    text-decoration: none;
    font-size: 1em;
    border-radius: 3px;
    border: none;
    background: #EF4444;
  }

  .collapsible-trigger:focus,
  .collapsible-trigger:active,
  .collapsible-trigger:hover {
    background: #F87171;
  }
</style>
