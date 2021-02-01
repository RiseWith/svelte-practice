
<script>
    export let left = 130;
    export let top = 130;
    let moving = false;

    function start(){
      moving = true;
    }

    function stop(){
      moving = false;
    }

  function move(e){
    if (moving) {
      left += e.movementX;
      top += e.movementY;
    }
  }

  $: console.log(moving);
</script>

<style>
  .draggable {
    user-select: none;
    position: absolute;
    border: solid 1px gray;
    cursor: move;
  }
</style>

<svelte:window on:mouseup={stop} />
<section on:mousedown={start} style="left: {left}px; top: {top}px;" class="draggable">
  <slot></slot>
</section>
