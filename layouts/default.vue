<template>
	<div>
		<Header />
		<div class="max-w-7xl mt-3 mx-auto">
	      	<Nuxt />
	    </div>
	</div>
</template>

<style>
	* {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
		font-family: sans-serif;
	}

	body {
	  background-color: #EEE;
	}

	a {
		text-decoration: none;
	}

	p {
		margin-bottom: 15px;
	}

	p:last-of-type {
		margin-bottom: 0px;
	}
</style>

<!-- <template>
  <div class="min-h-screen w-screen pt-24">
    <div class="max-w-7xl mx-auto">
      <Nuxt />
    </div>
  </div>
</template>
<script>
export default {}
</script> -->