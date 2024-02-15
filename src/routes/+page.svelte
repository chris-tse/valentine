<script>
	let size = $state(1)
	let firstNoClick = $state(false)

	function growYesButton() {
		firstNoClick = true
		size = size + 0.8
	}
</script>

<p class="big top-title">will u be my valentine?</p>
<div class="img-wrapper">
	<img src="/sampo.gif" alt="" />
</div>
{#if !firstNoClick}
	<p class="small">(u can try saying no)</p>
{/if}
<div class="button-container">
	<a class="btn" href="/yes" id="yes" style="font-size: {size}em; background: #22C55E">Yes</a>
	<button class="btn" on:click={growYesButton} style="background: #EF4444">No</button>
</div>

<style>

	img {
		width: 300px;
		height: auto;
	}

	.img-wrapper {
		margin: -20px auto;
		height: 300px;
	}

	.small {
		font-size: 0.8em;
	}

	.button-container {
		display: flex;
		justify-content: space-between;
	}

	#yes {
		transition: 0.2s;
	}

	button {
		border: none;
		align-self: flex-start;
		margin-left: 10px;

	}
	.btn {
		padding: 10px 8px;
		color: white;
		text-decoration: none;
		font-size: 1em;
		border-radius: 3px;
		touch-action: manipulation;
	}
</style>
