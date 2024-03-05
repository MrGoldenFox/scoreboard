<script>
	let countHome = 0;
	let countGuest = 0;

	function addHome1() {
		countHome += 1;
	}

	function addHome2() {
		countHome += 2;
	}

	function addHome3() {
		countHome += 3;
	}

	function addGuest1() {
		countGuest += 1;
	}

	function addGuest2() {
		countGuest += 2;
	}

	function addGuest3() {
		countGuest += 3;
	}

    function reset() {
        countGuest = 0;
        countHome = 0;
    }
</script>

<section>
	<div class="homeSection">
		<h1>HOME</h1>
		<p id="sumHome">{countHome}</p>
		<div class="addPoints">
			<button on:click={addHome1}>+1</button>
			<button on:click={addHome2}>+2</button>
			<button on:click={addHome3}>+3</button>
		</div>
	</div>
	<div class="controlPanel">
		<button on:click={reset}>RESET</button>
	</div>
	<div class="guestSection">
		<h1>GUEST</h1>
		<p id="sumGuest">{countGuest}</p>
		<div class="addPoints">
			<button on:click={addGuest1}>+1</button>
			<button on:click={addGuest2}>+2</button>
			<button on:click={addGuest3}>+3</button>
		</div>
	</div>
</section>

<style>
	@import url('https://fonts.cdnfonts.com/css/cursed-timer-ulil');

	@font-face {
		font-family: 'Verdana';
		src: url('../../../static/fonts/Verdana.ttf') format('truetype');
	}

	section {
		width: 100%;
		height: 100vh;
		background-color: #1b244a;
		display: flex;
		justify-content: center;
		align-items: center;
		text-align: center;
		gap: 3em;
	}

	h1 {
		color: #eeeeee;
		font-weight: 700;
		font-size: 2.5rem;
		line-height: 2.243125rem;
		font-family: 'Verdana', sans-serif;
	}

	p {
		margin: 0px 0px 40px 0px;
		color: #f94f6d;
		font-weight: 400;
		font-size: 5.625rem;
		line-height: 126.67px;
		background-color: #080001;
		width: 155px;
		height: 120px;
		border-radius: 5px;
		font-family: 'Cursed Timer ULiL', sans-serif;
	}

	.addPoints button {
		color: #9aabd8;
		font-weight: 400;
		font-size: 1.1rem;
		line-height: 27.81px;
		background-color: transparent;
		border: #9aabd8 solid 2px;
		border-radius: 5px;
		width: 45px;
		height: 45px;
		font-family: 'Cursed Timer ULiL', sans-serif;
	}

	.addPoints {
		display: flex;
		gap: 10px;
	}

	.addPoints button:hover {
		background-color: #2c355d;
	}

	.addPoints button:active {
		background-color: #0f162d;
	}

	.controlPanel button {
		width: 105px;
	    height: 35px;
        background: #2C355D;
        color: #FFFFFF;
        border: none;
        font-size: 1em;
        border-radius: 5px;
	}

    .controlPanel button:hover {
        background-color: #33408C;
    }

    .controlPanel button:active {
        background-color: #1F2B60;
    }

    @media only screen and (max-width: 600px){
        .controlPanel{
            position: absolute;
            bottom: 50px;
        }
    }

</style>
