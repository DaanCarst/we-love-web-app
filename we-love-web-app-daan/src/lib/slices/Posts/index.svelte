<script>
	/** @type {import("@prismicio/client").Content.PostsSlice} */
	export let slice;
  </script>
  
  <section>
	{#each slice.items as item}
		<h2>{item.link.data.title}</h2>
		<p></p>
	{/each}
  </section>
