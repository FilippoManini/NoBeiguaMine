<script>
	import Hero from "../lib/components/head.svelte";
	import News from "../lib/collection/news.svelte";
	import MediaQuery from "$lib/Utility/MediaQuery.svelte";
	import titanium from "../images/timeline/amianto01.png";
</script>

<div class="main">
		<Hero />

		<MediaQuery query="(min-width: 900px)" let:matches>
			{#if matches}
			<div class="root desktop">
				<div class="mdc-typography--headline3 title"> - Cronistoria - </div>
            	<div class="mdc-typography--body1 subTitle">del giacimento di titanio nel parco del beigua</div>
				<!-- FIRST SECTION -->
                <div class="section first">
                    <div class="column">
                        <div class="node-left">
                            <div class="mdc-typography--headline2 date">1970</div>
                            <div class="mdc-typography--body1 subDate"><strong>Scoperta del giacimento</strong> di quasi 400 milioni di tonnellate di rutilo, forma mineralogica con la quale si presenta il <strong>titanio</strong>, a Piampaludo.</div>
                        </div>
                    </div>
                    
                    <div class="column">
                        <div class="node-middle">
							<img class="image-container" id="scroller" src={titanium} alt="titanium"/>
                        </div>
                    </div>
                    

                    <div class="column">
                        <div class="node-right">
                            <div class="mdc-typography--headline2 date">1976</div>
                            <div class="mdc-typography--body1 subDate">Il ministero dell'industria rilascia alla Mineraria Italiana Srl una <strong>concessione ventennale</strong>, poi trasferita alla Compagnia Europea per il Titanio (C.E.T.), ma il <strong>progetto non parte</strong> per le proteste dei cittadini e delle istituzioni locali, che considerano l'operazione troppo rischiosa per salute e ambiente.</div>
                        </div>
                    </div>
                </div>
				<div class="more_timeline">
					<div class="buttom">
						<a class="text_b" href="/timeline">Mostra tutto</a>
					</div>
				</div>
	
			</div>
			{/if}
		</MediaQuery>
		
		<MediaQuery query="(max-width: 899px)" let:matches>
			{#if matches}
			<div class="root mobile">
				<div class="mdc-typography--headline4 title"> - Cronistoria - </div>
            	<div class="mdc-typography--body2 subTitle">del giacimento di titanio nel parco del beigua</div>
				<!-- FIRST SECTION -->
				<div class="section first">
					<div class="column">
						<div class="node-left">
							<div class="mdc-typography--headline2 date">1970</div>
							<div class="mdc-typography--body1 subDate"><strong>Scoperta del giacimento</strong> di quasi 400 milioni di tonnellate di rutilo, forma mineralogica con la quale si presenta il <strong>titanio</strong>, a Piampaludo.</div>
						</div>
					</div>
					
					<div class="column">
						<div class="node-middle">
							<img class="image-container" src={titanium} alt="titanium" style="width: 200px; height:200px; margin-left:50px;"/>
						</div>
					</div>

					<div class="column">
						<div class="node-right">
							<div class="mdc-typography--headline2 date">1976</div>
							<div class="mdc-typography--body1 subDate">Il ministero dell'industria rilascia alla Mineraria Italiana Srl una <strong>concessione ventennale</strong>, poi trasferita alla Compagnia Europea per il Titanio (C.E.T.), ma il <strong>progetto non parte</strong> per le proteste dei cittadini e delle istituzioni locali, che considerano l'operazione troppo rischiosa per salute e ambiente.</div>
						</div>
					</div>
				</div>
				<div class="more_timeline">
					<div class="buttom">
						<a class="text_b" href="/timeline">Mostra tutto</a>
					</div>
				</div>
			</div>
			{/if}
		</MediaQuery> 

		<News />
</div>

<style>
	.title{ 
		text-align: center;
		margin-top: 70px;
		margin-bottom: 15px;
        font-family:'Oswald',sans-serif;
        font-weight: 400;
		text-transform: uppercase;
		letter-spacing: 3px;
	}
	.subTitle{ 
        text-align: center;
        margin-bottom: 70px;
        font-family:'Roboto',sans-serif;
        font-size: larger;
    }

	.image-container{
        width: 100%;
        height: 100%;
    }

    /* Create three equal columns that floats next to each other */
    .desktop .column {
        float: left;
        width: 33.33%;
        height: auto;
    }

    .mobile .column{
        float: left;
        width: 100%;
        height: 25%;
		justify-content: center;
    }

    .section{
        border-radius: 50px 50px 0 0;
    }

    /* Clear floats after the columns */
    .section:after {
        content: "";
        display: table;
        clear: both;
    }

    .first{
        background-color:#557B83;
    }

	.desktop .date{
        font-family:'Oswald',sans-serif;
        font-weight: 1000;
        margin: 0 0 5% 0;
    }

    .desktop .subDate{
        font-family:'Roboto',sans-serif;
        font-size: larger;
    }

    .mobile .date{
        font-family:'Oswald',sans-serif;
        font-weight: 1000;
        margin: 0% 0% 5% 0%;
    }

    .mobile .subDate{
        font-family:'Roboto',sans-serif;
        font-size: larger;
    }

	/* DESKTOP */
	.desktop .node-left{
        margin: 21% 0% 0% 20%; /*21% 0% 0% 20%;*/
        font-family:'Roboto',sans-serif;
        color: white;
    }

    .desktop .node-middle{
        margin: 65% 33% 0% 25%; /*65% 33% 0% 25%;*/
        align-items: center;
    }

    .desktop .node-right{
        margin: 100% 20% 21% 0%; /*100% 20% 33% 0%;*/
        font-family:'Roboto',sans-serif;
        color: white;
    }

    /* MOBILE */
    .mobile .node-left{
        margin: 17% 10% 17% 10%; /*33% 0% 0% 20%;*/
        font-family:'Roboto',sans-serif;
        color: white;
    }

    .mobile .node-middle{
        margin: 0% 0% 0% 0%; /*33% 33% 0% 33%;*/
        align-items: center;
    }

    .mobile .node-right{
        margin: 17% 10% 17% 10%; /*83% 20% 33% 0%;*/
        font-family:'Roboto',sans-serif;
        color: white;
    }

	/* BUTTON */
	.more_timeline {
        text-align: center;
        margin: -15px 0 0 0;
        padding-top: 0px;
        padding-bottom: 70px;
		background-color:#557B83;
    }
    .buttom {
        background-color: white;
        border: none;
        color: rgb(0, 0, 0);
        padding: 10px 20px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 2px 1px;
        cursor: pointer;
        padding-bottom: 15px;
    }
    .text_b {
        font-family: "Oswald", sans-serif;
        text-decoration: none;
        color: black;
		text-transform: uppercase;
		letter-spacing: 3px;
    }
    .text_b,
    a:visited {
        color: black;
    }


</style>
