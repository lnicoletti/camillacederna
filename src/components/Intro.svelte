<script>
</script>

<main>
	<section id="intro">
		<div class="title">
			<div class="name"><h1>Camilla<br>Maria<br>Cederna</h1></div>
			<!-- svelte-ignore a11y-missing-attribute -->
			<div class="bioImage">
				<img src="images/camilla_cederna.jpg" alt="Bio Pic" class="rounded"/> 
			</div>
		</div>
		<div>
			<span class="tags">Enseignante</span>
			<span class="tags">Chercheuse</span>
			<span class="tags">Poete</span>
		</div>
		<div id="bio">
			<p>Je suis enseignante-chercheuse en langue, littérature et civilisation italiennes à l'<a href="" target=__blank>Université Lille</a>. Ma recherche porte sur les transferts culturels, la circulation du théâtre italien à l'époque moderne, la traduction, l'écriture des femmes dans l'espace méditerranéen. 
			Je suis co-responsable du <a href="" target=__blank>LAI (Laboratoire Associé International)</a>, "L'écriture de l'exil au féminin. Le dialogue entre les langues, les cultures et les idées, dans l'espace européen et méditerranéen (XIXe-XXIe siècles)", en collaboration avec l'<a href="" target=__blank>Université de Rome, La Sapienza</a> (2018-2022).<br><br>
			Dans le cadre de ce laboratoire, je dirige le projet de recherche et d'édition des inédits d'<a href="" target=__blank>Elisa Chimenti</a> (Naples 1883-Tanger 1969). Je participe à des évènements et à des échanges poétiques et culturels avec le Maroc et en particulier avec la ville de Tanger. J'ai publié un recueil de poèmes bilingue <a href="" target=__blank>Esilio di voci/Voix d'exil</a> (ATI, Brescia, 2016), et je publie mes poèmes aussi dans des <a href="" target=__blank>revues</a>.
			</p>
		</div>
		<!-- <div style="display:flex">
			<span><a href="https://pro.univ-lille.fr/camilla-cederna/">Recherche</a></span>
			<span><a href="">LinkedIn</a></span>
		</div> -->
	</section>
</main>

<style>

	img.rounded {
	object-fit: cover;
	border-radius: 50%;
	height: 200px;
	width: 200px;
	margin-top: 80px;
	/* border:7px solid #ffa200; */
	}

	.title {
		display:flex;
		text-align: left;
		flex-direction: row;
		/* height:100px */
	}

	.name {
		width:70%
	}

	#bio {
		text-align: justify;
		font-size:18px;
		font-variation-settings: 'opsz' 144, 'slnt' 0, 'wdth' 100,'wght' 420,'GRAD' 0;
	}

	.tags {
		margin: 20px;
		font-family: 'Roboto Flex', sans-serif;
		color: rgb(81, 35, 155);
		font-size: 30px;
		/* font-weight: 250; */
		font-variation-settings: 'opsz' 144, 'slnt' 0, 'wdth' 85,'wght' 470,'GRAD' -25,'YOPQ' 60,'YTUC' 703;

	}

	#intro {
		max-width: 50vw;
		margin: auto;
		text-align: center;
	}
	main {
		text-align: center;
		padding: 1em;
		/* max-width: 240px; */
		margin: 0 auto;
	}

	h1 {
		color: rgb(58, 5, 143);
		text-transform: uppercase;
		font-size: 4em;
		/* font-weight: 540;
		font-stretch: 33.3%; */
		font-family: 'Roboto Flex', sans-serif;
		font-variation-settings: 'opsz' 144,'wdth' 95,'wght' 520,'GRAD' 150,'YOPQ' 60,'YTUC' 703;
		
	}

	@media (max-width: 640px) {
		#intro {
			max-width: none;
		}
	}
	
	@media (max-width: 820px) {
		.title {
			display:flex;
			text-align: center;
			flex-direction: column;
			/* height:100px */
		}
		.name {
			width:100%
		}

		img.rounded {
			/* object-fit: cover;
			border-radius: 50%; */
			height: 150px;
			width: 150px;
			margin-top: 10px;
			margin-bottom: 20px;
			/* border:7px solid #ffa200; */
		}

		h1 {
			margin-bottom: 15px;
		}
	}
</style>