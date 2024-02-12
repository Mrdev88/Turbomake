<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/lightly.webp';
	import welcome_fallback from '$lib/images/lightly.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Turbomake Website" />
</svelte:head>

<section>
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>

		Turbomake
	</h1>

	<h2>
		<a href="https://turbomake.github.io">Create</a>
	</h2>
<a href="https://info.flagcounter.com/shI5"><img src="https://s11.flagcounter.com/count2/shI5/bg_FFFFFF/txt_000000/border_2328CC/columns_2/maxflags_10/viewers_0/labels_1/pageviews_1/flags_0/percent_0/" alt="Flag Counter" border="0"></a>
	<Counter />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
