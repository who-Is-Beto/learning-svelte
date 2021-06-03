<script>
	let product = {
		id: '',
		name: '',
		description: '',
		category: '',
		imageURL: '',
	}

	const handleSubmit = (event) => {
		event.preventDefault()
		console.log(event)
	}

</script>

<main>
	<form on:submit={handleSubmit}>
		<input 
			type="text" 
			placeholder="Product name" 
			bind:value={product.name}
		/>
		<textarea 
			bind:value={product.description}
			id="product-description" 
			rows="3" 
			placeholder="product Description..."
		/>

		<input 
		type="url" 
		id="product-image-url" 
		placeholder="https:yourimage.com"
		bind:value={product.imageURL}
		/>
		
		<select bind:value={product.category} id="category">
			<option value="laptops">laptops</option>
			<option value="servers">servers</option>
			<option value="PC">PC</option>
		</select>
		<button>save product!</button>
	</form>
</main>

<style>
</style>