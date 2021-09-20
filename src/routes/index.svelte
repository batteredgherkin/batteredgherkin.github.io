<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Counter from '$lib/Counter.svelte';
	import LinkImage from '$lib/LinkImage.svelte';
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section>
	<div class="welcome">
	<img src="/portrait.png" alt=""></div>
	<div class="hello"><h1>HALLO!</h1></div>

	<h2 class="subtitle">
		ich bin <strong>Ronja</strong>, Informatik-Studentin und Zeichnerin
	</h2>
	<h2 style="margin-top: 4rem">
		Hier sind ein paar Dinge, mit denen ich mich beschäftige:
	</h2>
	<div class="container">
		<LinkImage title="Stilisierung von 3D-Punktwolken" link="/aboutMe" src="/pointcloud.png"/>
		<LinkImage title="Skizzen und Lichtstudien" link="/aboutMe" src="/light_study.png"/>
		<LinkImage title="Zeichenserie bekannter Informatikerinnen" link="/aboutMe" src="/wit.png"/>
	</div>

</section>

<style>
	.container{
		padding:2rem;
		width: 90vw;
		padding-top:1rem;
		display: flex;
		flex-wrap: wrap;
		justify-content: space-evenly;
	}

	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
		margin-top:5rem;
	}

	h1 {
		width: 100%;
		margin:0 0;
		font-size: min(15vw, 200px);
		margin-right: max(-6vw,-100px);
		letter-spacing: min(6vw,100px);
		text-shadow: 0 0 min(4vw, 50px) var(--tertiary-color),0 0 min(4vw, 50px) var(--tertiary-color);
		
	}
	.subtitle {
		font-size: min(max(4vw, 2.25rem),4rem);
	}
	.hello {
		max-width: 1500px;
		position:relative;
		align-content: center;
	}

	.welcome {
		position: relative;
		width: 100%;
		height: min(45vw,23rem);
		z-index: -1;
		/*padding: 0 0 calc(100% * 495 / 2048) 0;*/
	}

	.welcome img {
		position: relative;
		width: 100%;
		top: 0;
		display: block;
	}
</style>
