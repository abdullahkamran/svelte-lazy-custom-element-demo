<script>
	export let name = "Default Name";
	let firstName = "";

	$: firstName = name.split(" ")[0];
</script>

<svelte:options tag="my-component" />
<main>
	<h4>Name: {name}!</h4>
	<h5>First name is: {firstName}</h5>
</main>
