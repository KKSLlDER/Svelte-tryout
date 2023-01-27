<script>
	let counter = 0;
	function increaseCounter() {
		counter += 10;
		document.querySelector('.error').classList.add('hidden');
	}
	function decreaseCounter() {
		if (counter > 0) {
			counter -= 10
			
			
		} else {
			document.querySelector('.error').classList.remove('hidden');
		}
	}
</script>
<div>
    <h1>OVN</h1>
    <div class="bg-shade">
        <p>{counter}°</p>
        <p class="hidden error">Can't go below 0!</p>
    </div>
    
    <div class="center">
        <button on:click={decreaseCounter}>-</button>
        <button on:click={increaseCounter}>+</button>
    </div>
</div>
<style>
    .bg-shade{
        background-color: #4b5563;
        opacity: 60%;

        margin-left: 40rem;
        margin-right: 40rem;
        padding-top: 20px;
        padding-bottom: 20px;
        margin-bottom: 20px;
    }
	:global(body) {
		background-image: url(/Child.png) !important;
		background-repeat: no-repeat;
		background-size: cover;
		background-position: 0px -600px;
	}
	button {
		padding: 20px;
	}
	.center {
		justify-content: center;
		width: 100%;
		display: flex;
		gap: 20px;
	}
	h1 {
		color: white;
		font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
		font-weight: lighter;
		font-size: 100px;
		text-align: center;
	}

	p {
		font-weight: 600;
		text-align: center;
		color: red;
		font-size: 50px;
		font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS',
			sans-serif;
	}
	.hidden {
		display: none;
	}
</style>
