<script>
	import SectionWrapper from './SectionWrapper.svelte';
	let faqs = [
		{
			question: 'What is Losos?',
			ans: 'Losos is a fun fitness app designed to make your workouts enjoyable by incorporating interactive games and challenges.'
		},
		{
			question: 'How do I download Losos?',
			ans: 'You can download Losos from the App Store (for iOS) or Google Play Store (for Android) on your mobile device.'
		},
		{
			question: 'Is Losos free to use?',
			ans: 'Yes, Losos offers a free version with basic features. There is also a premium subscription that unlocks additional games and advanced workout tracking.'
		},
		{
			question: 'What types of workouts does Losos offer?',
			ans: 'Losos offers a variety of workouts, including cardio, strength training, and flexibility exercises. The workouts are designed to be engaging and entertaining.'
		},
		{
			question: 'Can I connect Losos to my fitness tracker?',
			ans: 'Yes, Losos supports integration with popular fitness trackers, allowing you to sync your workout data and track your progress seamlessly.'
		},
		{
			question: 'Are there multiplayer features in Losos?',
			ans: 'Yes, Losos includes multiplayer challenges, allowing you to compete with friends or join group workouts for a more interactive and social experience.'
		},
		{
			question: 'How does Losos motivate users to stay active?',
			ans: 'Losos employs a reward system, where users earn points and achievements for completing workouts. These rewards can be used to unlock new levels, challenges, and in-app content.'
		},
		{
			question: 'Can I customize my workouts in Losos?',
			ans: 'Absolutely! Losos allows users to customize their workouts based on personal preferences, fitness goals, and available equipment.'
		},
		{
			question: 'Is there a beginner-friendly mode in Losos?',
			ans: 'Yes, Losos offers a beginner-friendly mode with easier exercises and lower intensity workouts, making it suitable for users at various fitness levels.'
		},
		{
			question: 'How often should I use Losos for optimal results?',
			ans: 'The frequency of Losos workouts depends on your fitness goals. It is recommended to engage in at least 3-5 sessions per week for noticeable results.'
		}
	];
</script>

<SectionWrapper id="faqs">
	<div class="flex flex-1 flex-col items-center justify-center gap-10 py-20 sm:gap-14 md:gap-24">
		<div class="flex flex-col gap-2">
			<p class="text-center text-base opacity-60 sm:text-lg md:text-xl">For all yout questions, qualms & queries</p>
			<h3 class="mx-auto w-full max-w-[1000px] text-center text-4xl font-semibold sm:text-5xl md:text-6xl">Frequently Asked Questions</h3>
		</div>
		<div class="flex w-full flex-col gap-8 sm:gap-10 md:gap-14">
			{#each faqs as faq}
				<div class="relative mx-auto flex w-full max-w-[800px] flex-col gap-2 p-4 px-6 text-left">
					<div class="absolute left-0 top-0 h-[1px] w-1/3 -translate-x-4 bg-slate-950"></div>
					<div class="absolute left-0 top-0 h-2/3 w-[1px] -translate-y-4 bg-slate-950"></div>
					<h4 class="pt-2 text-lg sm:text-xl md:text-2xl">{faq.question}</h4>
					<p class="pl-2">{faq.ans}</p>
				</div>
			{/each}
		</div>
	</div>
</SectionWrapper>
