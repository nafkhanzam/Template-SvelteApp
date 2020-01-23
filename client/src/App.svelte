<script>
	import Test from "./Test.svelte";
	import Home from "./Home.svelte";
	import NotFound from "./NotFound.svelte";
	import Router from 'svelte-spa-router'

	export let name;
	
	let routes = {
		'/': Home,
		// Exact path
		'/test': Test,
		'*': NotFound
	}
</script>
<div>
	<a href="#/test"><h1>Hello {name}!</h1></a>
	<a href="#/"><h1>Hello HOME!</h1></a>
	<a href="#/LMAO"><h1>Hello RANDOM!</h1></a>
</div>
<Router {routes}/>
