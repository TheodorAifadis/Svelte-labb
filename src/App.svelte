<script>
	let count1 = 0;
	let count2 = 0;
	let count3 = 0;
	let count4 = 0;
	let count5 = 0;
	let count6 = 0;
	let count7 = 0;
	let count8 = 0;
	let count9 = 0;
	let count10 = 0;
	let budget = 0;

	function hyra() {
		count1 = count1 + 500;
		budget = budget - 500;
	}

	function försäkring() {
		count2 = count2 + 500;
		budget = budget - 500;
	}

	function el() {
		count3 = count3 + 500;
		budget = budget - 500;
	}

	function internet() {
		count4 = count4 + 500;
		budget = budget - 500;
	}

	function mobil() {
		count5 = count5 + 500;
		budget = budget - 500;
	}

	function mat() {
		count6 = count6 + 500;
		budget = budget - 500;
	}

	function hygien() {
		count7 = count7 + 500;
		budget = budget - 500;
	}

	function transport() {
		count8 = count8 + 500;
		budget = budget - 500;
	}

	function nöjen() {
		count9 = count9 + 500;
		budget = budget - 500;
	}

	function sparande() {
		count10 = count10 + 500;
		budget = budget - 500;
	}

	function reset() {
		count1 = 0;
		count2 = 0;
		count3 = 0;
		count4 = 0;
		count5 = 0;
		count6 = 0;
		count7 = 0;
		count8 = 0;
		count9 = 0;
		count10 = 0;
		budget = 0;
		removeMoneyInput()
	}

	function onMoney(a) {
		let data = document.getElementById("money")
		budget = data.value
	}

	function removeMoneyInput() {
		let data = (document.getElementById("money").value = "")
	}
</script>

<main>
	<h1>Månadsbudget</h1>

	<h2>{budget} kr</h2>

	<input
		type="number"
		pattern="[0-9]"
		value=""
		placeholder="Budget"
		id="money"
		on:input={onMoney}
		style="display: block;align-self: center;margin-bottom: 20px; margin-right: auto;margin-left: auto;"
	/>

	<button on:click={hyra}>Hyra: {count1}kr</button>

	<button on:click={försäkring}>Försäkring: {count2}kr</button>

	<button on:click={el}>El: {count3}kr</button>

	<button on:click={internet}>Internet: {count4}kr</button>

	<button on:click={mobil}>Mobil: {count5}kr</button>

	<p />

	<button on:click={mat}>Mat: {count6}kr</button>

	<button on:click={hygien}>Hygien: {count7}kr</button>

	<button on:click={transport}>Transport: {count8}kr</button>

	<button on:click={nöjen}>Nöjen: {count9}kr</button>

	<button on:click={sparande}>Sparande: {count10}kr</button>

	<p />
	<button on:click={reset}>Återställ</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: darkgreen;
		text-transform: uppercase;
		font-family: "Times New Roman", Times, serif;
		font-size: 4em;
		font-weight: 100;
	}

	h2 {
		color: darkgreen;
		font-family: "Times New Roman", Times, serif;
		font-size: 3em;
		font-weight: 100;
	}

	button {
		color: darkgreen;
		font-family: "Times New Roman", Times, serif;
		font-size: 2em;
		font-weight: 100;
		background-color: whitesmoke;
		border: darkgreen;
		border-style: double;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
