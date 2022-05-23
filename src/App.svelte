<script>
	import Intro from "./components/Intro.svelte";
	import Recherche from "./components/Recherche.svelte";
	import Enseignement from "./components/Enseignement.svelte";
	import Ecriture from "./components/Ecriture.svelte";
	import Photographie from "./components/Photographie.svelte";
	import CV from "./components/CV.svelte";
	import Footer from "./components/Footer.svelte";
	import Media from "./components/Media.svelte";
	import Header from "./components/Header.svelte";
	import { onMount } from "svelte";
	import { csv, autoType} from "d3";

	let cvData;
	let categories = ['recherche', 'enseignement', 'ecriture', 'photographie', 'CV', 'media'];
	let selectedCategory;

	onMount(async () => {

		cvData = await csv("https://docs.google.com/spreadsheets/d/e/2PACX-1vQy5tSca4GLTvcQZctP9INF-vWzKjwBM5UI0SBJCJ8QuXvP_9vW17VQlKOziORUKiO_SYlwBmWG9o4y/pub?gid=1401498990&single=true&output=csv", autoType);

		console.log(cvData)
		
	});

	

</script>

<main>
	<Header/>
	<Intro/>
	<section>
		<div>
			{#each categories as data, i}
			<button class="tags" value={data} on:click={()=>{
				selectedCategory=data
				console.log(selectedCategory)
				}}>
				{data}
			</button>
			{/each}
		</div>
	</section>
	{#if selectedCategory==="recherche"}
		<Recherche/>
	{:else if selectedCategory==="CV"}
		<CV {cvData}/>
	{:else if selectedCategory==="enseignement"}
		<Enseignement/>
	{:else if selectedCategory==="ecriture"}
		<Ecriture/>
	{:else if selectedCategory==="photographie"}
		<Photographie/>
	{:else if selectedCategory==="media"}
		<Media/>
	{/if}
	<Footer/>
</main>

<style>

	img.rounded {
	object-fit: cover;
	border-radius: 50%;
	height: 200px;
	width: 200px;
	margin-top: 80px;
	}

	.title {
		display:flex;
		text-align: left;
		/* height:100px */
	}

	.name {
		width:70%
	}

	#bio {
		text-align: justify;
	}

	button {
		margin: 20px;
		margin-bottom: 20px;
		font-family: "Roboto flex", sans-serif;
		color: rgb(58, 5, 143);
		font-size: 20px;
		background-color: inherit;
		padding:0px;
		border: None;
		cursor:pointer;
		text-transform: capitalize;
		font-variation-settings: 'opsz' 144, 'slnt' 0, 'wdth' 85,'wght' 470,'GRAD' 30,'YOPQ' 60,'YTUC' 703;

	}

	button:hover {
		color: #ffa200;
	}

	button:focus {
		color: #ffa200;
		font-weight: 600px;
	}

	#intro {
		max-width: 50vw;
		margin: auto;
		text-align: center;
	}
	main {
		text-align: center;
		/* padding: 1em; */
		/* max-width: 240px; */
		margin: 0 auto;
	}


	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>