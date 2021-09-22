<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
	import SvelteSeo from "svelte-seo";
	let title = "Ronja Wagner";
	let description = "Ich bin Ronja Wagner, ich studiere IT-Systems Engineering mit einer Leidenschaft für Computergrafik und zeichne in meiner Freizeit. Auf dieser Seite gebe ich einen Einblick darin, womit ich mich beschäftige."
</script>
<SvelteSeo 
{title}
{description}
openGraph={{
 title: title,
 description: description,
 url: 'https://ronja-wagner.com',
 type: 'website',
 images: [{ url: 'https://ronja-wagner.com/portrait.png', alt: 'An drawing of myself' }]
}}
/>
<Header />

<main>
	<slot />
</main>

<footer>
	<p><a href="mailto:ronja.wagner@student.hpi.de">E-Mail</a> – <a href="https://de.linkedin.com/in/ronja-wagner">LinkedIn</a> – <a href="https://t.me/batteredgherkin">Telegram</a></p>
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
