<script>
  export let link;
  export let title;
  export let summary;
</script>

<div class="card">
  <h1>{title}</h1>
  <h2>{summary}</h2>

  <a href="{link}"><h3>LINK</h3></a>

  <slot />
</div>
