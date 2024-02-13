<script>
	export let index;
	export let productFeature;
</script>

<div class="relative grid grid-cols-1 gap-20 text-base md:grid-cols-2 md:gap-14 lg:gap-20">
	<div class={'flex flex-col gap-8 pt-8 sm:pt-10 md:gap-10' + (index % 2 === 1 ? ' md:order-2' : '')}>
		<h4 class="relative w-full max-w-[1000px] text-2xl font-medium after:absolute after:left-0 after:top-full after:mt-1 after:h-1.5 after:w-1/5 after:bg-slate-900 sm:text-3xl md:text-4xl">
			<slot />
		</h4>
		<p>{productFeature.description}</p>
		<div class="flex flex-col gap-3">
			{#each productFeature.featureList as listItem}
				<div class="flex items-center gap-2">
					<div class="grid aspect-square place-items-center rounded-full border-[1.5px] border-solid border-green-300 bg-white px-1.5 text-xs sm:text-sm">
						<i class="fa-solid fa-bolt text-green-400"></i>
					</div>
					<p>{listItem}</p>
				</div>
			{/each}
		</div>
		<div class="flex items-center">
			<button class="specialBtnDark mr-auto font-semibold">
				<p>Try Free To Today &rarr;</p>
			</button>
		</div>
	</div>
	<div class="dropShadow flex flex-col overflow-hidden rounded-b-lg">
		<div class="flex h-8 items-center gap-2 rounded-t-xl bg-white px-3 opacity-60 sm:h-10">
			{#each [1, 2, 3] as i}
				<div class="aspect-square w-2.5 rounded-full bg-indigo-300 sm:w-3" />
			{/each}
		</div>
		<div class="flex flex-1 flex-col gap-4 bg-white">
			<img src={productFeature.imgUrl} alt="product-img" />
		</div>
	</div>
</div>
