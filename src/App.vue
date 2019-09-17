<template>
  <div id="app">
	<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
	  <a class="navbar-brand" href="#">Navbar</a>
	  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarColor01" aria-controls="navbarColor01" aria-expanded="false" aria-label="Toggle navigation">
		<span class="navbar-toggler-icon"></span>
	  </button>

	  <div class="collapse navbar-collapse" id="navbarColor01">
		<ul class="navbar-nav mr-auto">
		  <li class="nav-item active">
			<router-link class="nav-link" to="/">Home <span class="sr-only"></span></router-link>
		  </li>
		  <li class="nav-item">
			<router-link class="nav-link" to="/blog">Blog</router-link>
		  </li>
		  <li class="nav-item">
			<router-link class="nav-link" to="/services">Services</router-link>
		  </li>
		  <li class="nav-item">
			<router-link class="nav-link" to="/contact">Contact</router-link>
		  </li>
		</ul>
		<form class="form-inline my-2 my-lg-0">
		  <input class="form-control mr-sm-2" type="text" placeholder="Search">
		  <button class="btn btn-secondary my-2 my-sm-0" type="submit">Search</button>
		</form>
	  </div>
	</nav>
	
    <transition name="moveInUp">
         <router-view/>
	</transition>
	
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

.moveInUp-enter-active{
  animation: fadeIn 1s ease-in;
}
@keyframes fadeIn{
  0%{
    opacity: 0;
  }
  50%{
    opacity: 0.5;
  }
  100%{
    opacity: 1;
  }
}

.moveInUp-leave-active{
  animation: moveInUp .3s ease-in;
}
@keyframes moveInUp{
 0%{
  transform: translateY(0);
 }
  100%{
  transform: translateY(-400px);
 }
}

</style>
