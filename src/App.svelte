<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import Sobre from "./routes/About.svelte";
  import Downloads from "./routes/Downloads.svelte";

  export let url = "";
</script>

<Router {url}>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <Link class="navbar-brand" to="/">PVNT21 <i class="bi bi-cpu"></i></Link>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarTogglerDemo02"
        aria-controls="navbarTogglerDemo02"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon" />
      </button>
      <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <Link class="nav-link" to="/">Home <i class="bi bi-house-fill"></i></Link>
          </li>
          <li class="nav-item">
            <Link class="nav-link" to="/sobre">Sobre <i class="bi bi-info-circle-fill"></i></Link>
          </li>
          <li class="nav-item">
            <Link class="nav-link" to="/downloads">Downloads <i class="bi bi-cloud-arrow-down-fill"></i></Link>
          </li>
          <li class="nav-item">
            <Link class="nav-link" to="/sc">Super-Chat <i class="bi bi-chat-left-text-fill"></i></Link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <!--  -->
  <div>
    <Route path="/" component={Home} />
    <Route path="sobre" component={Sobre} />
    <Route path="downloads" component={Downloads} />
  </div>
</Router>
