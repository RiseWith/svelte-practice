<script>
	import Router from "./Router.svelte";
	import Route from "./Route.svelte";

	import Home from "./Home.svelte";
	import Foo from "./Foo.svelte";
	import Bank from "./Bank.svelte";
</script>

	<Router hashbang ={false}>
		<Route path="/"><Home /></Route>
		<Route path="/foo"><Foo /></Route>
		<Route path="/bank"><Bank /></Route>
	</Router>
