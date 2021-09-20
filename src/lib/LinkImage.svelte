<script>
	export let link;
	export let title = "";
	export let src = "static/quad_placeholder.png";
</script>

<a href="{link}" aria-label="{title}"><div style='--bg-img: url("{src}")'><h1>{title}</h1></div></a>


<style lang="css">

    div{
        padding: 2.5rem;
        width: max(20vw, 12rem);
        height: max(20vw, 12rem);
        background-size: cover;
        position:relative;
        background-image: var(--bg-img);
    transition: 0.3s;
    }
    a{
        margin:1rem;
    }
    h1 {
        display: none;
    transition: 0.3s;
    }
    div:hover h1{
        display: unset;
        color: var(--tertiary-color);
        text-shadow: 0 0 0.5rem var(--heading-color), 0 0 0.5rem var(--heading-color), 0 0 0.5rem var(--heading-color);
        position:absolute;
        bottom:0rem;
        left:0;
        text-align: center;
        margin:10%;
        word-wrap: break-words;
        line-height: 2rem;
    }
    div:hover {
        padding: 2.5rem;
        box-shadow: inset 0 0 0 1000px var(--primary-color-transparent);
    }
</style>