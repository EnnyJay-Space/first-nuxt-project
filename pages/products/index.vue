<template>
	<div>
		<div class="grid grid-cols-4 gap-5">
			<div v-for="p in products">
				<ProductCard :product="p" />

				<!-- <NuxtLink :to="`/products/${p.id}` " class="font-bold">{{ p.title }}</NuxtLink> -->
			</div>
		</div>
	</div>
</template>

<script setup>
    definePageMeta({
        layout: 'products'
    })

    // fetch the products
    const { data: products } = await useFetch('https://fakestoreapi.com/products')

	// useHead({
	// 	title: 'nuxt dojo | Merch',
	// 	meta: [
	// 		{name:'description', content:'Nuxt 3 Merch'}
	// 	]
	// })
</script>

<style scoped>

</style>