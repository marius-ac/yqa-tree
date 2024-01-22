<script>
    export let showModal = false;
    export let close = () => {};
  
    // Add any props or methods needed for node configuration here
  </script>
  
  {#if showModal}
  <div class="modal-overlay" on:click={close}>
    <div class="modal" on:click|stopPropagation>
      <!-- Node configuration form goes here -->
      <button on:click={close}>Close</button>
    </div>
  </div>
  {/if}
  
  <style>
    .modal-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.5);
      display: flex;
      align-items: center;
      justify-content: center;
    }
  
    .modal {
      background: white;
      padding: 1rem;
      border-radius: 4px;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
    }
  </style>
  