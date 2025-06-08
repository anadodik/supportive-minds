<script>
	import { writable } from 'svelte/store';
	import { page } from '$app/stores';
	import { ExternalLink } from 'lucide-svelte';

	import { Tabs, Accordion } from '@skeletonlabs/skeleton-svelte';

	let group = $state('about');
	const accordion = $state(['Gender Affirming Care']);
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
	<header class="bg-primary-500 flex flex-col md:flex-row justify-center md:items-end gap-4 lg:h-[11em] pb-4 lg:pr-4">
		<div class="lg:absolute flex flex-row justify-center items-center gap-4 max-w-screen-md">
			<div class="flex flex-col justify-center items-center gap-0">
				<img src="Secondary Logo_White.svg" class="w-96 object-scale-down" alt="Supportive Minds PLLC. Logo"/>
				<p class="text-center p-0 text-xl"><span class="text-white">Supporting Change, Reducing Harm</span></p>
			</div>
		</div>
		<div class="lg:ml-auto">
			<div class="spwidget-button-wrapper"><a href="https://supportiveminds.clientsecure.me" class="spwidget-button" data-spwidget-scope-id="2f8b8601-b2df-4ba7-bc74-8cb0768ed708" data-spwidget-scope-uri="supportiveminds" data-spwidget-application-id="7c72cb9f9a9b913654bb89d6c7b4e71a77911b30192051da35384b4d0c6d505b" data-spwidget-scope-global data-spwidget-autobind>Request Free Consultation</a></div>
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
			<img alt="Katherine Clemens and Zoi Andalcio" class="w-full h-auto bg-surface-500 rounded-3xl" src="kath-n-zoi-2.jpg" />
			<h3 class="p-8 h3 text-center">
				<span class="text-primary-500">Our Offerings</span>
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
					{#snippet control()}Community Plus{/snippet}
					{#snippet panel()}
						<p class="font-serif">
							For those in need of care beyond just psychotherapy, we offer a combined care team that includes  a combination of case management, home management, community outreach and psychotherapy provided by both of our clinicians for around 5 service hours per week. This service is billed at a set monthly rate and includes both in office and in community support. Thorough consultation and case review are included to best support those who may be in need of more than a therapist can offer individually. 
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
			<h3 class="p-8 h3 text-center">
				<span class="text-primary-500">Fees</span>
			</h3>
			<!-- <br/> -->
			<div class="card variant-soft-primary shadow-lg border-soft-primary border-[1px] p-12 overflow-hidden block">
				<!-- <div class="p-4 pl-12 pr-12 flex flex-col lg:flex-row items-center justify-start space-x-4"> -->
					<p>
						All of our services are considered out-of-network with insurance carriers, meaning that clients pay out of pocket for all services rendered because some of the services we provide are outside of traditional medical model practice and are non-reimbursable. The out-of-network structure allows us the flexibility to provide more intensive, individualized, and unique care. We will provide a monthly superbill that can be used to submit claims to your insurance carrier for partial reimbursement for those who have out-of-network benefits. The reimbursement rate for each individual plan differs so we encourage you to reach out to your insurance carrier beforehand to see what the reimbursement rate will be. We are happy to help with the process and can ensure that we will provide you with accurate, timely superbills and transparency around costs up front. 
					</p>
					<br/>
					<p>
						All individual psychotherapy and case management sessions are billed at $200 per 50min session. For meetings that occur in the community, we bill travel time at 15min prorated increments of $200. Services beyond psychotherapy and case management are billed on an individual basis depending on hours of service and the type of care needed. Individual and agency training costs are calculated based on the size of attendance and the training requested. Please reach out to us directly at <a href="mailto:inquiries@supportivemindscounseling.com">inquiries@supportivemindscounseling.com</a> to review the exact costs for the additional services we offer. 
					</p>
					<br/>
					<p>
						We offer a limited number of sliding scale spaces for individuals who otherwise would not be able to afford our fees. Priority for these spaces are given to those who hold a <b>gender diverse</b> or <b>BIPOC</b> identity. 
					</p>
					<p>
						Payment is accepted via check, credit card, or hsa/fsa. 
					</p>
					<br/>
					<!-- </div> -->
			</div>
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
						<p class="text-md whitespace-nowrap text-nowrap">
							Email us: 
							<a class="text-secondary-500" href="mailto:kclemens@supportivemindscounseling.com">
								inquiries@supportivemindscounseling.com
							</a><br/>
							Call us:
							<a class="text-secondary-500" href="mailto:kclemens@supportivemindscounseling.com">
								(617) 858-5996
							</a><br/>
							<span class="inline-flex gap-2">
							Follow us on social media:
							<a class="text-secondary-500 text-center" href="https://bsky.app/profile/supportiveminds.bsky.social">
								<svg class="w-6 fill-secondary-500" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--!Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.--><path d="M111.8 62.2C170.2 105.9 233 194.7 256 242.4c23-47.6 85.8-136.4 144.2-180.2c42.1-31.6 110.3-56 110.3 21.8c0 15.5-8.9 130.5-14.1 149.2C478.2 298 412 314.6 353.1 304.5c102.9 17.5 129.1 75.5 72.5 133.5c-107.4 110.2-154.3-27.6-166.3-62.9l0 0c-1.7-4.9-2.6-7.8-3.3-7.8s-1.6 3-3.3 7.8l0 0c-12 35.3-59 173.1-166.3 62.9c-56.5-58-30.4-116 72.5-133.5C100 314.6 33.8 298 15.7 233.1C10.4 214.4 1.5 99.4 1.5 83.9c0-77.8 68.2-53.4 110.3-21.8z"/></svg>
							</a>
							<a class="text-secondary-500 text-center" href="https://www.linkedin.com/company/106497222/admin/dashboard/">
								<svg class="w-6 fill-secondary-500" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--!Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.--><path d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z"/></svg>
							</a>
							</span>
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
						<div class="spwidget-button-wrapper"><a href="https://supportiveminds.clientsecure.me" class="spwidget-button" data-spwidget-scope-id="2f8b8601-b2df-4ba7-bc74-8cb0768ed708" data-spwidget-scope-uri="supportiveminds" data-spwidget-application-id="7c72cb9f9a9b913654bb89d6c7b4e71a77911b30192051da35384b4d0c6d505b" data-spwidget-scope-global data-spwidget-autobind>Request Free Consultation</a></div>
						<script src="https://widget-cdn.simplepractice.com/assets/integration-1.0.js"></script>
						<!-- End SimplePractice Appointment-Request Widget Embed Code -->
						<br/>
						<hr class="opacity-80" />
						<div class="p-4 pl-8 pr-12 flex items-center justify-center space-x-4">
							<h3 class="h3" data-toc-ignore><span class="text-primary-500">Where To Find Us</span></h3>
						</div>
						<iframe title="Office location on Google Maps" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2946.2200945297927!2d-71.1293754236272!3d42.40175807118904!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89e3771e01397e9f%3A0xc0db7d4b9e561c5e!2s206%20Holland%20St%2C%20Somerville%2C%20MA%2002144!5e0!3m2!1sen!2sus!4v1739659982357!5m2!1sen!2sus" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
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
					<img alt="Katherine Clemes and Zoi Andalcio" class="w-48 h-auto bg-surface-500 rounded-full" src="kath-n-zoi.jpg" />
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
						<br/>
						<p>
							To us, practicing harm reduction goes beyond providing tools for safer consumption. It is about resisting practices that take away bodily autonomy and dignity of risk.
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
					<img alt="Katherine Clemens" class="w-48 h-auto bg-surface-500 rounded-full" src="kath.jpg" />
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
								My approach to therapy is person-centered, collaborative, empowerment-focused, and rooted in evidence-based practices. I strive to create a therapeutic space grounded in curiosity rather than judgment. As a harm reduction-oriented therapist, I draw from extensive training in Integrated Harm Reduction Psychotherapy, Motivational Interviewing, Mentalization-Based Therapy, Community Reinforcement and Family Training (CRAFT), and other contextual and person-centered modalities.
							</p>
							<br/>
							<p>	
								My work is centered on creating safe, inclusive, and affirming spaces—especially for individuals marginalized by the stigma surrounding mental illness, substance use, high-risk behaviors, race, gender, and differing political realities. I believe in using the tools of mental health and psychology to support social justice and collective liberation. I work closely with people who use substances and navigate complex co-occurring medical and psychiatric challenges. At the core of my practice is a commitment to helping people feel truly seen, and to supporting their journey toward self-efficacy, healing, and empowerment.
							</p>
							<br/>
							<p>
								To sustain my work, I prioritize two things; my health and my family.  I enjoy staying active through engaging in physical exercise and different wellness practices. I'm grateful to share my life with my wife and our children.
							</p>
							<br/>
							<p>

							</p>
						</article>
					</section>
					<img alt="Zoi Andalcio" class="w-48 h-auto bg-surface-500 rounded-full" src="zoi.jpg" />
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
				<Tabs.Control value="about" classes="pb-1 pt-1" stateActive="border-primary-500 border-b-[3px]" labelClasses="hover:preset-tonal-secondary">About</Tabs.Control>
				<Tabs.Control value="services" classes="pb-1 pt-1" stateActive="border-primary-500 border-b-[3px]" labelClasses="hover:preset-tonal-secondary">Offerings & Fees</Tabs.Control>
				<Tabs.Control value="contact"classes="pb-1 pt-1"  stateActive="border-primary-500 border-b-[3px]" labelClasses="hover:preset-tonal-secondary">Contact</Tabs.Control>
				<a href="https://supportiveminds.clientsecure.me/sign-in"><Tabs.Control value="clients" disabled="true" classes="pb-1 pt-1" labelClasses="hover:preset-tonal-secondary">{#snippet lead()}<ExternalLink size={22}/>{/snippet}Existing Client Portal</Tabs.Control></a>
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
		<p class="text-xs">
			We are committed to providing an inclusive therapeutic space for all identities and remain steadfast in supporting the dismantlement of cultural and institutional barriers that prevent good mental health for all people. We also want to acknowledge that we are on Native land. We denounce the erasure of Native history, culture and people that is both historical and ongoing.
			We acknowledge that our therapy practice is located on Naumkeag, Pawtucket and Massachusett native land.
		</p>
	</section>

	<a href="https://www.inclusivetherapists.com/massachusetts/somerville/zoi-andalcio?from=badge" title="Find me on Inclusive Therapists" target="_blank" class="w-24 p-0 m-0 mt-0">
		<img alt="Inclusive Therapists" src="https://www.inclusivetherapists.com/images/inclusive_therapists_members_badge.png" class="w-12 object-scale-down p-0"/>
	</a>
	<img src="pride.png" class="w-12 object-scale-down" alt="Pride Flag"/>
	<p class="w-fit whitespace-nowrap">Supportive Minds Counseling PLLC.</p>
</footer>
</div>
