<script>
  import Modal from "./Modal.svelte";
  let modal;
</script>

<style>
  textarea {
    width: 100%;
    height: 90vh;
    background-color: pink;
  }
</style>

<main>
  <textarea />
  <button on:click={() => modal.show()}>Show modal</button>
  <Modal bind:this={modal}>
    <h2>Modal title</h2>
    <p>Modal content.</p>
    <button on:click={() => modal.hide()}>Close</button>
  </Modal>
</main>
