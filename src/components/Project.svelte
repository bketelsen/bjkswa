<script>
  export let github;
  export let title;
  export let summary;
</script>

<div class="card">
  <h1>{title}</h1>
  <h2>{summary}</h2>
  {#if {github} }
  <a href="{github}"><h3>GitHub</h3></a>
  {/if}
  <slot />
</div>
