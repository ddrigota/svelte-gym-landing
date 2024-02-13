<script>
	import SectionWrapper from './SectionWrapper.svelte';
	import Header from './Header.svelte';
	import CtAs from './CTAs.svelte';
</script>

<SectionWrapper>
	<Header />
	<div class="flex flex-1 flex-col items-center justify-center gap-10 pb-10 md:pb-14">
		<h2 class="mx-auto w-full max-w-[1200px] text-center text-5xl font-semibold sm:text-6xl md:text-7xl lg:text-8xl">
			<span class="text-indigo-400">Gym</span> Training
			<span class="text-slate-600 line-through">Is Hard</span><br />
			Just Got <span class="text-indigo-400">Easier</span>
		</h2>
		<p class="mx-auto w-full max-w-[1000px] text-center text-xl sm:text-2xl md:text-3xl">
			Less thinking & more doing. We're the trainer in your pocket full of <span class="italic">personaloized workouts, exercise, explanations, analytics</span> and much much more.
		</p>
		<CtAs />
		<div class="flex items-center justify-center gap-2 text-base">
			<p class="">4.6</p>
			{#each [0, 1, 2, 3, 4] as index}
				<div class="relative grid place-items-center">
					<i class="fa-solid fa-star opacity-0"></i>
					<div class={'absolute left-0 top-0 grid place-items-center ' + (index === 4 ? 'w-3/5 overflow-hidden' : ' ')}>
						<i class="fa-solid fa-star text-amber-400"></i>
					</div>
				</div>
			{/each}
			<p>500+</p>
		</div>
	</div>
</SectionWrapper>
