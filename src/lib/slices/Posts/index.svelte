<script>
	/** @type {import("@prismicio/client").Content.PostsSlice} */
	export let slice;
  </script>
  <body>
	<section class="content-container">
		<h1>Daan's blog post</h1>
		{#each slice.items as item}
			<section class="item-container">
				<h2>{item.link.data.title}</h2>
				<p>{item.link.data.content}</p>
				<p class="author">{item.link.data.auteur}</p>
			</section>
		{/each}
	</section>
  </body>

<style>

	.content-container {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		gap: 1em;
		color: var(--c-white);
		padding: 1em;
		margin: 1em;
	}

	.content-container>*:first-child {
		align-self: center;
	}

	.item-container {
		background-color: var(--c-container);
		padding: 2em;
		border-radius: 30px;
		max-width: 45em;
		letter-spacing: .05em;
	}

	h1 {
		color: var(--c-magenta);
	}

	h2 {
		color: var(--c-magenta);
		margin-bottom: .5em;
	}

	.author {
		font-size: .8em;
		margin-top: 1em;
	}


</style>
