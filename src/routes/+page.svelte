<script>
	import { writable } from 'svelte/store';
	import { page } from '$app/stores';
	import { ExternalLink } from 'lucide-svelte';

	import { Tabs, Accordion } from '@skeletonlabs/skeleton-svelte';

	let group = $state('about');
	const accordion = $state(['Gender Affirming Care']);

	const tabSet = writable(0);
	
</script>

<style>
	.spwidget-button-wrapper{
		text-align: center
	}
	.spwidget-button{
		display: inline-block;
		padding: 12px 24px;
		color: #fff !important; 
		background: rgb(192 148 87);
		border: 0;
		border-radius: 4px;
		font-size: 16px;
		font-weight: 600;
		text-decoration: none;
	}
	.spwidget-button:hover{
		background: rgb(70 40 0);
		color: rgb(192 148 87);
	}
	.spwidget-button:active{
		color: rgb(192 148 87) !important;
		box-shadow: 0 1px 3px rgba(0, 0, 0, .15) inset
	}
</style>

<div class="grid grid-rows-[auto_1fr_auto]">
	<header class="bg-primary-500 flex flex-col md:flex-row justify-center md:items-end gap-4 lg:h-[10em] pb-4 lg:pr-4">
		<div class="lg:absolute flex flex-row justify-center items-center gap-4 max-w-screen-md">
			<img src="Secondary Logo_White.svg" class="w-96 object-scale-down" alt="Supportive Minds PLLC."/>
		</div>
		<div class="lg:ml-auto">
			<div class="spwidget-button-wrapper"><a href="https://supportiveminds.clientsecure.me" class="spwidget-button" data-spwidget-scope-id="2f8b8601-b2df-4ba7-bc74-8cb0768ed708" data-spwidget-scope-uri="supportiveminds" data-spwidget-application-id="7c72cb9f9a9b913654bb89d6c7b4e71a77911b30192051da35384b4d0c6d505b" data-spwidget-scope-global data-spwidget-autobind>Request Appointment</a></div>
		</div>
	</header>
	
	{#snippet services()}
	<div class="container mx-auto grid grid-cols-1 xl:grid-cols-[100px_minmax(0px,_1fr)_100px]">
		<aside class="sticky top-0 col-span-1 hidden min-h-[50vh] p-4 xl:block"></aside>
		<main class="col-span-1 space-y-4 p-2 min-h-[50vh] flex justify-center">
			<div class="flex flex-col w-full">
			<!-- <div class="card p-2 m-2 mb-12 variant-soft-primary shadow-xl overflow-hidden block">
				<div class="p-2 flex items-center justify-start">
				<section class="text-primary-500">
					<article>
						<p class="font-serif">
							Are you stuck in the pattern of behaviors that you want to change but do not know how to stop/lessen? 
							Are the most vulnerable student athletes not accessing mental health services on your college campus? 
							Are you worried about your child’s exposure or use of substances?
							Are you looking for psychological evaluation for gender affirming medical care?
						</p>
					</article>
				</section>
				</div>
			</div> -->
			<img class="w-full h-auto bg-surface-500 rounded-3xl" src="kath-n-zoi-2.jpg" />
			<h3 class="p-8 h3 text-center">
				<span class="text-primary-500">Our Services</span>
			</h3>
			<br/>
			<hr class="hr"/>
			<Accordion {accordion} multiple>
				<Accordion.Item controlHover="hover:preset-tonal-secondary" value="Specialized and Individualized Addiction Counseling">
					<!-- {#snippet lead()}X{/snippet} -->
					{#snippet control()}Specialized and Individualized Addiction Counseling{/snippet}
					{#snippet panel()}
						<p class="font-serif">
						Supportive Minds specializes in working with individuals in an outpatient setting who are actively engaged in risky behaviors that may be disqualified from getting services elsewhere. We are highly trained in modalities that uplift client autonomy and reduce harm so change can be possible. We work with adolescents and adults. 
						</p>
					{/snippet}
				</Accordion.Item>
				<hr class="hr" />
				<Accordion.Item controlHover="hover:preset-tonal-secondary" value="Collegiate Athlete Mental Wellness Coaching">
					<!-- {#snippet lead()}X{/snippet} -->
					{#snippet control()}Collegiate Athlete Mental Wellness Coaching{/snippet}
					{#snippet panel()}
						<p class="font-serif">
							Student-athletes are at a higher risk than their non-athlete peers for certain mental health challenges, including substance use, eating disorders, depression, and social or performance anxiety. Supportive Minds can help by collaborating with counseling centers and athletic departments to create a campus environment that prioritizes mental wellbeing. This includes efforts to destigmatize mental illness within athletic programs and developing processes for identifying and referring students who require clinical support as well as by providing direct mental health services to student-athletes through targeted workshops and individualized care. We are dedicated to supporting the mental well-being of student-athletes and ensuring they have the resources they need to thrive both on and off the field.
						</p>
					{/snippet}
				</Accordion.Item>
				<hr class="hr" />

				<Accordion.Item controlHover="hover:preset-tonal-secondary" value="Gender-affirming surgery assessment and letter writing">
					<!-- {#snippet lead()}X{/snippet} -->
					{#snippet control()}Gender-affirming surgery assessment and letter writing{/snippet}
					{#snippet panel()}
						<p class="font-serif">
						Sessions for evaluation, understanding informed consent and exploration of treatment options are available for those pursuing gender affirming medical care. 
						</p>
					{/snippet}
				</Accordion.Item>
				<hr class="hr" />

				<Accordion.Item controlHover="hover:preset-tonal-secondary" value="Adolescent Services">
					<!-- {#snippet lead()}X{/snippet} -->
					{#snippet control()}Adolescent Services{/snippet}
					{#snippet panel()}
						<p class="font-serif">
							We offer individual counseling for adolescents ages 12-18, with a specialized focus on navigating identity confusion and addressing high-risk behaviors commonly associated with distress during this critical developmental stage.
						</p>
					{/snippet}
				</Accordion.Item>
				<hr class="hr" />

				<Accordion.Item controlHover="hover:preset-tonal-secondary" value="Parent Coaching">
					<!-- {#snippet lead()}X{/snippet} -->
					{#snippet control()}Parent Coaching{/snippet}
					{#snippet panel()}
						<p class="font-serif">
							Our parent coaching is based on the CRAFT method, Community Reinforcement and Family Training. Supportive Minds uses the CRAFT method to assist care givers/ guardians/ parents to better communicate with their children struggling with addictive processes and assist in helping them set boundaries for self-care. 
						</p>
					{/snippet}
				</Accordion.Item>
				<hr class="hr" />

				<Accordion.Item controlHover="hover:preset-tonal-secondary" value="Clinical Case Management">
					<!-- {#snippet lead()}X{/snippet} -->
					{#snippet control()}Clinical Case Management{/snippet}
					{#snippet panel()}
						<p class="font-serif">
							We provide highly individualized and culturally sensitive community based case management to not only help manage and organize care but to also help people establish and connect to a community. Our case management services are built on principles of independence, dignity, and shared decision making where we emphasize the importance of meeting the individual where they are at, which may include meeting in the home or meeting in the community alongside the person as they work towards integration. 
						</p>
					{/snippet}
				</Accordion.Item>
				<hr class="hr" />

				<Accordion.Item controlHover="hover:preset-tonal-secondary" value="Training/Consultation">
					<!-- {#snippet lead()}X{/snippet} -->
					{#snippet control()}Training/Consultation{/snippet}
					{#snippet panel()}
						<p class="font-serif">
							We provide individualized, trauma-informed consultation and training to organizations looking to improve their literacy and agency practices around addiction psychology, gender and sexuality diversity, harm reduction, and student athlete mental health. 
						</p>
					{/snippet}
				</Accordion.Item>
				<hr class="hr" />
			</Accordion>
			</div>
		</main>
		<aside class="sticky top-0 col-span-1 hidden min-h-[50vh] p-4 xl:block"></aside>
	</div>
	{/snippet}

	{#snippet contact()}
	<div class="container mx-auto grid grid-cols-1 xl:grid-cols-[100px_minmax(0px,_1fr)_100px]">
		<aside class="sticky top-0 col-span-1 hidden min-h-[50vh] p-4 xl:block"></aside>
		<main class="col-span-1 space-y-4 p-2 min-h-[50vh] flex justify-center">
			<!-- Start SimplePractice Appointment-Request Widget Embed Code -->
			<!-- End SimplePractice Appointment-Request Widget Embed Code -->
			<div class="flex flex-col">
				<section class="h-full flex flex-col items-center justify-start text-center">
					<article class="">
						<h3 class="h3">
							<span class="text-primary-500">Contact Us</span>
						</h3>
						<p class="text-md">
							Email us: 
							<a class="text-secondary-500" href="mailto:kclemens@supportivemindscounseling.com">
								inquiries@supportivemindscounseling.com
							</a><br/>
							Call us:
							<a class="text-secondary-500" href="mailto:kclemens@supportivemindscounseling.com">
								(617) 858-5996
							</a>
							<!-- To email Zoi Andalcio:
							<a class="text-secondary-500" href="mailto:kclemens@supportivemindscounseling.com">
								zandalcio@supportivemindscounseling.com
							</a> -->
							<!-- <a class="text-secondary-500" href="https://maps.app.goo.gl/1mv9WNXgyJUFg2w7A">
								Supportive Minds,<br/>
								206 Holland St, <br/>
								Somerville, MA <br/>
							</a> -->
							<!-- kclemens@supportivemindscounseling.com -->
						</p>
						<br/>
						<!-- <h5 class="h5"> -->
						<p>
							To book a consultation directly:
						</p>
						<br/>
						<!-- </h5> -->
						<!-- Start SimplePractice Appointment-Request Widget Embed Code -->
						<div class="spwidget-button-wrapper"><a href="https://supportiveminds.clientsecure.me" class="spwidget-button" data-spwidget-scope-id="2f8b8601-b2df-4ba7-bc74-8cb0768ed708" data-spwidget-scope-uri="supportiveminds" data-spwidget-application-id="7c72cb9f9a9b913654bb89d6c7b4e71a77911b30192051da35384b4d0c6d505b" data-spwidget-scope-global data-spwidget-autobind>Request Appointment</a></div>
						<script src="https://widget-cdn.simplepractice.com/assets/integration-1.0.js"></script>
						<!-- End SimplePractice Appointment-Request Widget Embed Code -->
						<br/>
						<hr class="opacity-80" />
						<div class="p-4 pl-8 pr-12 flex items-center justify-center space-x-4">
							<h3 class="h3" data-toc-ignore><span class="text-primary-500">Where To Find Us</span></h3>
						</div>
						<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2946.2200945297927!2d-71.1293754236272!3d42.40175807118904!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89e3771e01397e9f%3A0xc0db7d4b9e561c5e!2s206%20Holland%20St%2C%20Somerville%2C%20MA%2002144!5e0!3m2!1sen!2sus!4v1739659982357!5m2!1sen!2sus" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
					</article>
					<!-- <button type="button" class="btn btn-2xl pt-5 pb-5 w-full h-1/4 bg-secondary-500 text-2xl drop-shadow-xl">Book Consultation</button> -->
				</section>
			</div>
		</main>
		<aside class="sticky top-0 col-span-1 hidden min-h-[50vh] p-4 xl:block"></aside>
	</div>
	{/snippet}

	{#snippet about()}
	<div class="container mx-auto grid grid-cols-1 xl:grid-cols-[50px_minmax(0px,_1fr)_50px]">
		<aside class="sticky top-0 col-span-1 hidden min-h-[50vh] p-4 xl:block"></aside>
		<main class="col-span-1 space-y-2 p-4 min-h-[50vh]">
			<div class="container mx-auto h-3/8 gap-4 flex flex-col lg:flex-row items-center justify-start">
				<!-- <div class="card variant-soft-primary h-full overflow-hidden"> -->
					<img class="w-48 h-auto bg-surface-500 rounded-full" src="kath-n-zoi.jpg" />
					<!-- <section class="p-4 h-full flex flex-col items-center justify-center text-center"> -->
					<!-- </section> -->
					<!-- <section class="p-4 h-full flex flex-col items-center justify-center text-center">
						<article class="p-2">
							<p class="text-md">
								<a class="text-secondary-500" href="https://maps.app.goo.gl/1mv9WNXgyJUFg2w7A">
									Supportive Minds,<br/>
									206 Holland St, <br/>
									Somerville, MA <br/>
								</a>
							</p>
						</article>

						<div class="spwidget-button-wrapper"><a href="https://supportiveminds.clientsecure.me" class="spwidget-button" data-spwidget-scope-id="2f8b8601-b2df-4ba7-bc74-8cb0768ed708" data-spwidget-scope-uri="supportiveminds" data-spwidget-application-id="7c72cb9f9a9b913654bb89d6c7b4e71a77911b30192051da35384b4d0c6d505b" data-spwidget-scope-global data-spwidget-autobind>Request Appointment</a></div>
						<script src="https://widget-cdn.simplepractice.com/assets/integration-1.0.js"></script> -->
					<!-- </section> -->
				<!-- </div> -->
				<!-- <div class="card variant-soft-primary overflow-hidden"> -->
					<article class="p-4">
						<h5 class="h5" data-toc-ignore> Who We Are </h5>
						<p class="font-serif">
							<!-- cspell:disable -->
							Supportive Minds is a specialty outpatient mental health and addiction practice dedicated to inclusivity, community, and harm reduction. We provide care to adults, adolescents, and traditionally underserved or vulnerable populations, utilizing a variety of evidence-based clinical models of care. Our services are available in-office, in the community, or virtually to best meet the needs of our clients. As a minority-owned business, we are proud to serve and uplift diverse communities.
							<!-- Supportive Minds is a specialty outpatient mental health and addiction practice with a focus on inclusivity, community, and harm-reduction.
							We provide services to adults, adolescents, and traditionally vulnerable and underserved populations and are are trained in various evidence-based clinical models of care.
							We meet our clients in our office space, in the community, or virtually.
							Supportive Minds is minority-owned business.
							<br/><br/>
							We are here to help support your mind, wellness and growth no matter where you are in your recovery journey. You deserve respect for your autonomy, human connection and a safe space where you can self actualize the change you want in your life.  -->
							<!-- Supportive Minds was founded by two clinicians passionate about providing community- and empowerment-oriented mental health services.  We are a specialty addictions/high-risk behaviors outpatient group practice that offers inclusive, harm-reduction-oriented addiction and mental health services. We service adult and adolescent populations that include traditionally vulnerable and underserved populations. We offer confidential and safe mental health services that are flexible and customized to our clients in the community, in our office space, or virtually on telehealth. We are trained in various evidence-based clinical models of care. We are a minority-owned business and proud to serve the people of Massachusetts.  -->
							<!-- cspell:enable -->
						</p>
						<br/>
						<p class="font-serif">
							At Supportive Minds, we are committed to supporting your mental health, wellness, and personal growth, wherever you may be on your recovery journey. You deserve respect for your autonomy, meaningful human connection, and a safe space to create the positive change you seek in your life.
						</p>
					</article>
				<!-- </div> -->
			</div>

			<hr class="opacity-80" />
			
			<!-- <div class="flex items-center justify-center"> -->
			<h2 class="h2 text-center pt-4" data-toc-ignore><span class="text-primary-500">Our Team</span></h2>
			<!-- </div> -->
			<div class="card variant-soft-primary shadow-lg border-soft-primary border-[1px] overflow-hidden block">
				<div class="p-4 pl-12 pr-12 flex flex-col lg:flex-row items-center justify-start space-x-4">
					<!-- <div class="placeholder-circle size-20 bg-surface-900 animate-pulse"></div> -->
					<img class="w-48 h-auto bg-surface-500 rounded-full" src="kath.jpg" />
					<section class="p-4">
						<h3 class="h3" data-toc-ignore>Katherine Clemens</h3>
						<p class="text-sm">Co-founder</p>
						<hr class="opacity-80"/>
						<article class="font-serif pt-4 pb-4">
							<p>
								I am passionate about working with individuals from all walks of life, with a particular focus on supporting teens and young adults who identify on the LGBTQ+ spectrum, as well as anyone feeling uncertain about their identity and purpose regardless of age, sexuality, and gender.
								<br/><br/>
								My practice is rooted in a relational, community-oriented approach, where I believe that connection and understanding are key drivers of healing and recovery. I bring experience in addressing a broad range of mental health concerns, including depression, anxiety, psychosis, mood disorders, and addiction/addictive processes.
								<br/><br/>
								I integrate an interpersonal and relational framework, focusing on identity, context, and values to meet the unique needs of each client. I do not subscribe to a one-size-fits-all model of healing; rather, I believe that each person’s journey is distinct. My work emphasizes Harm Reduction, Mentalization-Based Therapy, CBT, and Motivational Interviewing
								<br/><br/>
								In my free time I enjoy heavy music, boxing, oddities, and being outdoors with my dogs. 
							</p>
						</article>
					</section>
				</div>
			</div>
			<div class="card variant-soft-primary shadow-lg border-soft-primary border-[1px] overflow-hidden block">
				<div class="p-4 pl-12 pr-12 flex flex-col-reverse lg:flex-row items-center justify-start space-x-4">
					<section class="p-4 ">
						<h3 class="h3" data-toc-ignore>Zoi Andalcio</h3>
						<p class="text-sm">Co-founder</p>
						<hr class="opacity-80"/>
						<article class="font-serif pt-4 pb-4">
							<p>
								My approach to therapy is client centered, collaborative, empowerment oriented, and evidence based.  I am intentional about providing space for curiosity and not judgement. I am a harm reduction-oriented therapist who has been trained in Integrated Harm Reduction Psychotherapy, Motivational Interviewing, Mentalization Based Therapy, Community Reinforcement and Family Training and various other contextual and person-centered based modalities. 
							</p>
							<br/>
							<p>	
								My life's work is about curating a safe and welcoming environment for marginalized people; people who have been marginalized by the stigma of mental illness, addictions, various behaviors deemed as high-risk, race, sex and different political realities. I am committed to using the field of mental health and psychology to uplift social justice causes and actions to promote liberation for my clients. I have worked with people who use substances and who suffer from various different comorbidities including medical and psychiatric most of my career. Most importantly, I am here to help my clients feel seen and empowered to move to a place of self-efficacy.
							</p>
							<br/>
							<p>
								When I am not working as a psychotherapist and business owner I enjoy physical activities like running, hiking and strength training. I love watching sports, experiencing art and listening to music, especially live music. I am lucky enough to share my life with my wife and our children.
							</p>
							<br/>
							<p>

							</p>
						</article>
					</section>
					<img class="w-48 h-auto bg-surface-500 rounded-full" src="zoi.jpg" />
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
			<h2 class="h2">What we do</h2>
				<a href="https://supportiveminds.clientsecure.me/">Katherine's Portal</a>
				<!-- Start SimplePractice Appointment-Request Widget Embed Code -->
				<div class="spwidget-button-wrapper"><a href="https://supportiveminds.clientsecure.me" class="spwidget-button" data-spwidget-scope-id="2f8b8601-b2df-4ba7-bc74-8cb0768ed708" data-spwidget-scope-uri="supportiveminds" data-spwidget-application-id="7c72cb9f9a9b913654bb89d6c7b4e71a77911b30192051da35384b4d0c6d505b" data-spwidget-scope-global data-spwidget-autobind>Request Appointment</a></div>
				<script src="https://widget-cdn.simplepractice.com/assets/integration-1.0.js"></script>
				<!-- End SimplePractice Appointment-Request Widget Embed Code -->
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
				<Tabs.Control value="about" stateActive="border-primary-500 border-b-[3px]" labelClasses="hover:preset-tonal-secondary">About</Tabs.Control>
				<Tabs.Control value="services" stateActive="border-primary-500 border-b-[3px]" labelClasses="hover:preset-tonal-secondary">Services</Tabs.Control>
				<Tabs.Control value="contact" stateActive="border-primary-500 border-b-[3px]" labelClasses="hover:preset-tonal-secondary">Contact</Tabs.Control>
				<a href="https://supportiveminds.clientsecure.me/sign-in"><Tabs.Control value="clients" disabled="true" labelClasses="hover:preset-tonal-secondary">{#snippet lead()}<ExternalLink size={22}/>{/snippet}Existing Client Portal</Tabs.Control></a>
			</div>
			{/snippet}
			{#snippet content()}
				<Tabs.Panel value="about">
					{@render about()}
				</Tabs.Panel>
				<Tabs.Panel value="services">
					{@render services()}
				</Tabs.Panel>
				<Tabs.Panel value="contact">
					{@render contact()}
				</Tabs.Panel>
				<Tabs.Panel value="clients">
					<!-- {@render tabcontent()} -->
				</Tabs.Panel>
			{/snippet}
		</Tabs>

<!-- Footer -->
<footer class="bg-secondary-500 mt-8 p-4 flex flex-col gap-6 lg:flex-row items-center justify-end align-center text-center w-full">
	<section class="">
		<p class="">
			We are committed to providing an inclusive therapeutic space for all identities and remain steadfast in supporting the dismantlement of cultural and institutional barriers that prevent good mental health for all people. We also want to acknowledge that we are on Native land. We denounce the erasure of Native history, culture and people that is both historical and ongoing.
		</p>
	</section>

	<img src="pride.png" class="w-12 object-scale-down " alt="Pride Flag"/>
	<p class="w-fit whitespace-nowrap">Supportive Minds Counseling PLLC.</p>
</footer>
</div>
