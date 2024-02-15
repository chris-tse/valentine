<main>
    <slot/>
</main>

<style>
  main {
    font-family: Arial, sans-serif;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 15px;
  }

  :global(:root) {
    font-size: 20px;
  }

  :global(.big) {
    font-size: 1.2em;
  }

  :global(.top-title) {
    margin-top: 150px;
  }
</style>
