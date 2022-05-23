<script>
    export let cvData;
    import { descending } from "d3";
    console.log("test data", cvData)
    let data = cvData.sort((a,b) => descending(a.startYear, b.startYear));
</script>

<section>
    {#each data as d, i}
        <div>
            <span class="date">{d.startYear}</span> - <span class="date">{d.endYear==="null"?"current":d.endYear}</span>: {d.title}, <i>{d.org}</i>, {d.place}
        </div>
        <br>
    {/each}
</section>

<style>
    
section {
    width: 50vw;
	max-width: 500px;
    margin: auto;
    text-align: center;
}

div {
    text-align: left;
    font-size:18px;
	font-variation-settings: 'opsz' 144, 'slnt' 0, 'wdth' 100,'GRAD' 0;
}

.date {
    font-variation-settings: 'opsz' 144, 'slnt' 0, 'wght' 500, 'wdth' 100,'GRAD' 150;
    color:rgb(81, 35, 155)
}

h1 {
    color: rgb(5, 143, 113);
    /* text-transform: uppercase; */
    font-size: 5em;
    font-weight: 100;
    font-family: 'Square Peg', cursive
    
}

@media (max-width: 640px) {
    section {
        max-width: none;
    }
}
</style>