<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./components/Home.svelte";
  import About from "./components/About.svelte";
  import Gallery from "./components/Gallery.svelte";
</script>

<Router>
  <nav>
    <Link to="/">Home</Link>
    <Link to="/About">About</Link>
    <Link to="/Gallery">Gallery</Link>
  </nav>
  <div>
    <Route path="/"><Home /></Route>
    <Route path="/About"><About /></Route>
    <Route path="/Gallery"><Gallery /></Route>
  </div>
</Router>

<style>
	:global(*, body){
		box-sizing: border-box;
		margin: 0;
		padding: 0;
	}

	:global(body){
		background-color: rgb(0, 0, 0);
	}
	:global(main){
		margin-left: 20vw;
		min-height: 100vh;
    background-color: rgb(26, 26, 26); 
		display: flex;
		flex-direction: column;
    padding: 5% 0 0 10%; 
    color: white;
	}

	nav{
    position: fixed;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: start;
    justify-content: space-evenly;
    top: 0;
    left: 0;
    color: white;
    background-color: rgb(0, 0, 0);
    width: 20vw;
    height: 100vh;
  }
	
</style>