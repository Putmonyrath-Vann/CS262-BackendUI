<svelte:head>
	<title>Admin List</title>
	<meta name="List" content="Admin List" />
</svelte:head>


<script>
	// https://svelte.dev/examples#svelte-component
	// https://www.w3schools.com/howto/tryit.asp?filename=tryhow_js_full_page_tabs
	import user from './userTab.svelte';
	import hotel from './hotelTab.svelte';
	
	const webpages = [
		{ name: "User", component: user },
		{ name: "Hotel", component: hotel },
	];
	
	// Loads an object in webpages array
	let selectedPage = webpages[0];
	$: console.dir(selectedPage)
	
	// Have to use obj as arg. so value can be a class
	// @ts-ignore
	const tab = (obj) => selectedPage = obj;

</script>

<div class="margin">
	<div class="row">
		<div class="d-flex justify-content-center">
			<button class="tablink" title={webpages[0].name} on:click={() => tab(webpages[0])}>{webpages[0].name}</button>
			<button class="tablink" title={webpages[1].name} on:click={() => tab(webpages[1])}>{webpages[1].name}</button>
		</div>
	</div>
</div>
<!-- Loaded component/webpage -->
<svelte:component this={selectedPage.component} />


<style>

	.margin{
		margin-top: 25px;
	}

	/* Style tab links */
	.tablink {
		background-color: #ed1e1eb6;
		color: white;
		float: left;
		border: 1px solid #000000;
		border-radius: 0;
		font-size: 17px;
		width: 25%;
	}

	.tablink:active{
		background-color: white;
	}

	.tablink:hover {
		background-color: rgb(14, 50, 255);
	}

</style>