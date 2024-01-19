<script>

  import { Link, Router, Route } from 'svelte-routing';
import Images from './routes/images/page.svelte';
import Chat from './routes/chat/page.svelte';
import Home from './routes/Home.svelte';
export let url = "";
</script>

  <Router {url}>
    <nav class="bg-gray-800 p-4 text-white flex justify-between items-center">
      <div class="flex items-center">
        <a href="/" class="text-xl font-semibold">BedRock UI</a>
      </div>
      <div class="flex space-x-4">
        <Link to="/" class="hover:bg-gray-700 px-3 py-2 rounded-md">Home</Link>
        <Link to="/chat" class="hover:bg-gray-700 px-3 py-2 rounded-md">Chat</Link>
        <Link to="/images" class="hover:bg-gray-700 px-3 py-2 rounded-md">Images</Link>
      </div>
    </nav>
    <div>
      <Route path="/chat" component={Chat} />
      <Route path="/images" component={Images} />
      <Route path="/"><Home /></Route>
    </div>

  </Router>





