<script>
	export let name = "Default Name";
	let firstName = "";

	$: firstName = name.split(" ")[0];
</script>

<style>
	h2 {
		color: red;
	}
</style>

<svelte:options tag="my-component" />
<main>
	<h1>Name: {name}!</h1>
	<h2>First name is: {firstName}</h2>
</main>
