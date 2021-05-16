<script>
  export let title = "Header";
  export let left = 150;
  export let top = 150;

  let dragging = false;
  const start = () => {
    dragging = true;
  };

  const stop = () => {
    dragging = false;
  };

  const move = (e) => {
    if (dragging) {
      left += e.movementX;
      top += e.movementY;
    }
  };
</script>

<svelte:window on:mouseup={stop} on:mousemove={move} />

<section style="left: {left}px; top: {top}px" class="draggable">
  <div on:mousedown={start} class="header">{title}</div>
  <div class="content">
    <slot />
  </div>
</section>

<style>
  .draggable {
    position: absolute;
    user-select: none;
    border: 1px solid gray;
  }

  .header {
    cursor: move;
    padding: 8px;
    background-color: gray;
  }

  .content {
    padding: 8px;

    background-color: white;
  }
</style>
