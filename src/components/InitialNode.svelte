<script>
  import NodeConfigModal from './NodeConfigModal.svelte';
  let showModal = false;

  function handleDoubleClick() {
    showModal = true;
  }

  function closeModal() {
    showModal = false;
  }
    // Initial Node component logic goes here
  
    // Example: Node properties
    let id = 'node-1';
    let style = `position: absolute; left: 5%; top: 50%; transform: translateY(-50%);`;
  </script>
  
  <!-- Node HTML structure -->
  <div class="node" style={style}>
    <p>Initial Node</p>
    <!-- Add more UI elements as needed -->
  </div>
  

  <div class="node" on:dblclick={handleDoubleClick}>
    <!-- Node content -->
  </div>
  
  <NodeConfigModal {showModal} close={closeModal} />


  <style>
    .node {
      /* Adjusted positioning */
      position: absolute;
      top: 50%;
      left: 0;
      transform: translateY(-50%);
      
      /* Rest of your styles */
      border: 1px solid #333;
      padding: 10px;
      border-radius: 5px;
      background-color: white;
      text-align: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }
  </style>
  