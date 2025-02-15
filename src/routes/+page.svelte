<script>
	import { writable } from 'svelte/store';
	import { page } from '$app/stores';

	import { Tabs } from '@skeletonlabs/skeleton-svelte';
	let group = $state('about');

	const tabSet = writable(0);
</script>
<div class="grid grid-rows-[auto_1fr_auto]">
	<header class="bg-primary-500 p-4 flex flex-row justify-center items-center gap-4">
		<div class="flex flex-row justify-center items-center gap-4 max-w-screen-md">
			<!-- <div class="placeholder-circle size-20"></div>
			<h1 class="h1">Supportive Minds</h1> -->
			<img src="Secondary Logo_White.svg" class="w-96 object-scale-down" alt="Supportive Minds PLLC."/>
		</div>
	</header>

	{#snippet contact()}
	<div class="container mx-auto grid grid-cols-1 xl:grid-cols-[100px_minmax(0px,_1fr)_100px]">
		<aside class="sticky top-0 col-span-1 hidden min-h-[50vh] p-4 xl:block"></aside>
		<main class="col-span-1 space-y-4 p-4 min-h-[50vh] flex justify-center">
			<div class="flex flex-col">
				<div class="p-4 pl-8 pr-12 flex items-center justify-center space-x-4">
					<h2 class="h2" data-toc-ignore><span class="text-primary-500">Where To Find Us</span></h2>
				</div>
				<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2946.2200945297927!2d-71.1293754236272!3d42.40175807118904!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89e3771e01397e9f%3A0xc0db7d4b9e561c5e!2s206%20Holland%20St%2C%20Somerville%2C%20MA%2002144!5e0!3m2!1sen!2sus!4v1739659982357!5m2!1sen!2sus" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
			</div>
		</main>
		<aside class="sticky top-0 col-span-1 hidden min-h-[50vh] p-4 xl:block"></aside>
	</div>
	{/snippet}

	{#snippet about()}
	<div class="container mx-auto grid grid-cols-1 xl:grid-cols-[100px_minmax(0px,_1fr)_100px]">
		<aside class="sticky top-0 col-span-1 hidden min-h-[50vh] p-4 xl:block"></aside>
		<main class="col-span-1 space-y-4 p-4 min-h-[50vh]">
			<div class="container mx-auto grid grid-cols-6 h-3/8 gap-4 items-center">
				<!-- card-hover -->
				<div class="card col-span-2 variant-soft-primary h-full overflow-hidden">
					<section class="p-4 h-full flex flex-col items-center justify-center text-center">
						<article class="p-2">
							<p class="text-md">
								<a class="text-secondary-500" href="https://maps.app.goo.gl/1mv9WNXgyJUFg2w7A">
									Supportive Minds,<br/>
									206 Holland St, <br/>
									Somerville, MA <br/>
								</a>
								<!-- kclemens@supportivemindscounseling.com -->
							</p>
						</article>
						<button type="button" class="btn btn-2xl pt-5 pb-5 w-full h-1/4 bg-secondary-500 text-2xl drop-shadow-xl">Book Consultation</button>
					</section>
				</div>
				<!-- card-hover -->
				<div class="col-span-4 col-start-3 card variant-soft-primary overflow-hidden">
					<article class="p-4">
						<h5 class="h5" data-toc-ignore> Who We Are </h5>
						<p class="font-serif">
							<!-- cspell:disable -->
							Supportive Minds is a specialty outpatient mental health and addiction practice with a focus on inclusivity, community, and harm-reduction.
							We provide services to adults, adolescents, and traditionally vulnerable and underserved populations.
							We meet our clients in our office space, in the community, or virtually.
							We are trained in various evidence-based clinical models of care and are a minority-owned business. 
							<!-- Supportive Minds was founded by two clinicians passionate about providing community- and empowerment-oriented mental health services.  We are a specialty addictions/high-risk behaviors outpatient group practice that offers inclusive, harm-reduction-oriented addiction and mental health services. We service adult and adolescent populations that include traditionally vulnerable and underserved populations. We offer confidential and safe mental health services that are flexible and customized to our clients in the community, in our office space, or virtually on telehealth. We are trained in various evidence-based clinical models of care. We are a minority-owned business and proud to serve the people of Massachusetts.  -->
							<!-- cspell:enable -->
						</p>
						<!-- <h1 class="font-bold">Mission Statement</h1> -->
						<!-- <p class="font-serif"> -->
							<!-- cspell:disable -->
							<!-- We at Supportive Minds, PLLC believe in creating entry points for access to high-quality mental health services, especially for vulnerable populations (BIPOC, LGBTQ, and women).
							We believe in providing evidence-based harm-reduction-oriented treatment and support for high-risk behaviors.
							We believe in our duty to care and see ourselves in the suffering of others so that we may collectively listen, understand, and when possible, offer support toward empowerment and change. -->
							<!-- cspell:enable -->
						<!-- </p> -->
					</article>
				</div>
			</div>

			<hr class="opacity-80" />
			
			<div class="p-4 pl-8 pr-12 flex items-center justify-center space-x-4">
				<h2 class="h2" data-toc-ignore><span class="text-primary-500">Our Team</span></h2>
			</div>

			<div class="card variant-soft-primary shadow-xl overflow-hidden block">
				<div class="p-4 pl-12 pr-12 flex items-center justify-start space-x-4">
					<!-- <div class="placeholder-circle size-20 bg-surface-900 animate-pulse"></div> -->
					<img class="w-48 h-48 bg-surface-500 rounded-full" src="kath.png" />
					<section class="p-4">
						<h3 class="h3" data-toc-ignore>Katherine "Hottie Hot Pants" Clemens</h3>
						<p class="text-sm">Co-founder and hottie pants</p>
						<hr class="opacity-80"/>
						<article class="font-serif pt-4 pb-4">
							<p>
								<!-- cspell:disable -->
								Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam aspernatur provident eveniet eligendi cumque consequatur tempore
								sint nisi sapiente. Iste beatae laboriosam iure molestias cum expedita architecto itaque quae rem.
								<!-- cspell:enable -->
							</p>
						</article>
					</section>
				</div>
			</div>
			<div class="card variant-soft-primary shadow-xl overflow-hidden block">
				<div class="p-4 pl-12 pr-12 flex items-center justify-start space-x-4">
					<section class="p-4 ">
						<h3 class="h3" data-toc-ignore>Zoi Andalcio</h3>
						<p class="text-sm">Co-founder and lukewarm pants</p>
						<hr class="opacity-80"/>
						<article class="font-serif pt-4 pb-4">
							<p>
								<!-- cspell:disable -->
								Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam aspernatur provident eveniet eligendi cumque consequatur tempore
								sint nisi sapiente. Iste beatae laboriosam iure molestias cum expedita architecto itaque quae rem.
								<!-- cspell:enable -->
							</p>
						</article>
					</section>
					<img class="w-48 h-48 bg-surface-500 rounded-full" src="zoi.jpg" />
				</div>
			</div>
			<!-- </div> -->
		</main>
		<aside class="sticky top-0 col-span-1 hidden min-h-[50vh] p-4 xl:block"></aside>
	</div>
	{/snippet}

	{#snippet tabcontent()}
	<div class="container mx-auto grid grid-cols-1 xl:grid-cols-[100px_minmax(0px,_1fr)_100px]">
		<aside class="sticky top-0 col-span-1 hidden h-screen p-4 xl:block"></aside>

		<main class="col-span-1 space-y-4 p-4">
			<hr class="opacity-50 !border-t-1" />
			<a class="card card-hover overflow-hidden" href="#">
				<div class="w-full text-token grid grid-cols-3 md:grid-cols-3 gap-4">
					<button type="button" class="btn btn-xl bg-surface-500">BOOK CONSULTATION</button>
					<button type="button" class="btn btn-xl col-span-2 bg-surface-500">???</button>
				</div>
			</a>
			<h2 class="h2">What we do</h2>
			<div class="w-full text-token grid grid-cols-3 md:grid-cols-3 gap-4">
				<a class="card variant-soft-primary card-hover overflow-hidden" href="#">
					<header class="card-header"><img src="gay.jpeg" class="bg-black/50 w-full aspect-[21/9]" alt="Post" /></header>
					<section class="p-4">
						<h6 class="h6" data-toc-ignore>Gay</h6>
						<h3 class="h3" data-toc-ignore>We are gay!</h3>
						<article>
							<p>
								<!-- cspell:disable -->
								Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam aspernatur provident eveniet eligendi cumque consequatur tempore
								sint nisi sapiente. Iste beatae laboriosam iure molestias cum expedita architecto itaque quae rem.
								<!-- cspell:enable -->
							</p>
						</article>
					</section>
					<hr class="opacity-50" />
					<footer class="p-4 flex justify-start items-center space-x-4">
						<div class="flex-auto flex justify-between items-center">
							<!-- <h6 class="font-bold" data-toc-ignore>Find out more about being gay.</h6> -->
							<small>Find out more about being gay.</small>
						</div>
					</footer>
				</a>
				<a class="card variant-soft-primary card-hover overflow-hidden" href="#">
					<header class="card-header"><img src="needle.webp" class="bg-black/50 w-full aspect-[21/9]" alt="Post" /></header>
					<section class="p-4">
						<h6 class="h6" data-toc-ignore>Needles!</h6>
						<h3 class="h3" data-toc-ignore>We love drugs!</h3>
						<article>
							<p>
								<!-- cspell:disable -->
								Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam aspernatur provident eveniet eligendi cumque consequatur tempore
								sint nisi sapiente. Iste beatae laboriosam iure molestias cum expedita architecto itaque quae rem.
								<!-- cspell:enable -->
							</p>
						</article>
					</section>
					<hr class="opacity-50" />
					<footer class="p-4 flex justify-start items-center space-x-4">
						<div class="flex-auto flex justify-between items-center">
							<!-- <h6 class="font-bold" data-toc-ignore>Find out more about being gay.</h6> -->
							<small>Find out more about being gay.</small>
						</div>
					</footer>
				</a>

				<a class="card variant-soft-primary card-hover overflow-hidden" href="#">
					<header class="card-header"><img src="boutique.png" class="bg-black/50 w-full aspect-[21/9]" alt="Post" /></header>
					<section class="p-4">
						<h6 class="h6" data-toc-ignore>Boutique!</h6>
						<h3 class="h3" data-toc-ignore>Idk what this means</h3>
						<article>
							<p>
								<!-- cspell:disable -->
								Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam aspernatur provident eveniet eligendi cumque consequatur tempore
								sint nisi sapiente. Iste beatae laboriosam iure molestias cum expedita architecto itaque quae rem.
								<!-- cspell:enable -->
							</p>
						</article>
					</section>
					<hr class="opacity-50" />
					<footer class="p-4 flex justify-start items-center space-x-4">
						<div class="flex-auto flex justify-between items-center">
							<!-- <h6 class="font-bold" data-toc-ignore>Find out more about being gay.</h6> -->
							<small>Find out more about... clothing?</small>
						</div>
					</footer>
				</a>
			</div>
			<hr class="opacity-50 !border-t-1" />
			<p class="h-[100px] p-4">For inquiry contact Katherine Clemens, LICSW at kclemens@supportivemindscounseling.com or Zoi Andalcio, LMHC at zandalcio@supportivemindscounseling.com</p>
		</main>

		<!-- Sidebar (Right) -->
		<aside class="sticky top-0 col-span-1 hidden h-screen p-4 xl:block"></aside>
	</div>
	{/snippet}

		<Tabs bind:value={group} listClasses="bg-surface-500 justify-center items-center" fluid>
			{#snippet list()}
			<div class="container flex flex-row justify-center items-center max-w-screen-md">
				<Tabs.Control value="about">About</Tabs.Control>
				<Tabs.Control value="services">Services</Tabs.Control>
				<Tabs.Control value="contact">Contact</Tabs.Control>
				<Tabs.Control value="clients">Existing Clients</Tabs.Control>
			</div>
			{/snippet}
			{#snippet content()}
				<Tabs.Panel value="about">
					{@render about()}
				</Tabs.Panel>
				<Tabs.Panel value="services">
					{@render tabcontent()}
				</Tabs.Panel>
				<Tabs.Panel value="contact">
					{@render contact()}
				</Tabs.Panel>
				<Tabs.Panel value="clients">
					{@render tabcontent()}
				</Tabs.Panel>
			{/snippet}
		</Tabs>

<!-- Footer -->
<footer class="bg-secondary-500 mt-8 p-4 flex flex-row justify-end text-end w-full">
	<p>Supportive Minds Counseling PLLC.</p>
</footer>
</div>
