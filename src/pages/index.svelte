<div class="hero">
  <h1>Routify blog example</h1>
  <code>npx @sveltech/routify init --branch blog</code>
  
  <ul class="checks">
    <li>☑ Markdown with mdsvex</li>
    <li>☑ PostCSS</li>
    <li>☑ Auto generated navigation</li>
    <li>☑ Auto generated page titles</li>
    <li>☑ 100% Lighthouse score</li>
  </ul>

  {#if item }
  <div>
    {item}
  </div>
{:else}
  <!-- this block renders when photos.length === 0 -->
  <p>loading...</p>
{/if}
</div>

<script>
	import { onMount } from 'svelte';


	let item;
	onMount(async () => {
		const res = await fetch(`/api/message`);
		item = await res.json();
	});

</script>

<!-- routify:options index=10 -->
<!-- routify:options title="home" -->
