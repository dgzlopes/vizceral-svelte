<script>
  import Vizceral from "vizceral";
  import { onMount } from "svelte";
  let viz;
  let running = false;
  export let traffic;
  export let styles = {};
  export let filters = [];
  export let modes;

  onMount(async () => {
    setTimeout(function() {
      run();
    }, 100);
  });

  function run() {
    running = true;
    viz = new Vizceral(document.getElementById("vizceral"));
    viz.updateStyles(styles);
    viz.updateData(traffic);
    viz.setFilters(filters);
    viz.setModes(modes);
    viz.setView();
    viz.animate();
  }

  $: if (traffic && running) {
    viz.updateData(traffic);
  }

  $: if (styles && running) {
    viz.updateStyles(styles);
  }

  $: if (filters && running) {
    viz.setFilters(filters);
  }

  $: if (modes && running) {
    viz.setModes(modes);
  }
</script>

<canvas id="vizceral" />
