<template>
	<div class="home-header">
		<div class="flex-col xl:flex-row flex pb-8 justify-between">
			<div class="mr-4">
				<div class="row">
					<img class="home-header-logo" src="@/assets/logo.png" />
					<h1 class="home-header-name">Michael Webb</h1>
				</div>
				<div class="col mt-4">
					<h1 class="home-header-title">Make your next video pop.</h1>
					<h2 class="home-header-subtitle">Want a nice feel to your video? You’ve come
					to the right place.<br><br>

					Need captions? I got that for you too.</h2>
					<h2 class="home-header-scroll xl:mb-0 mb-4">Scroll down to learn more.</h2>
				</div>
			</div>
			<div class="home-header-iframe">
				<h2 class="xl:block hidden home-header-example">A playlist showcasing my recent work.</h2>
				<iframe src="https://www.youtube.com/embed/videoseries?list=PLzQ6psXMqCdfiXw0IeGPJkMe_G7na6EZt" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
			</div>
		</div>
	</div>
	<div class="home-content mt-12">
		<div class="col">
			<div class="xl:flex-row flex-col flex w-full">
				<img class="home-point-img" src="@/assets/img/ytvideo.jpg" />
				<div class="xl:m-10 mt-8">
					<h1 class="home-header-name ml-0-pls mb-2">It’s not just a video, it’s a story.</h1>
					<h2 class="home-point-desc mb-2">
						When you truly want to tell a story to your audience, you need the right
						editor who can place it together piece-by-piece. That’s why you need
						someone who’s been piecing together YouTube videos for over 8 years.
					</h2>
					<h2 class="home-point-footnote">Example shot from “A PC User’s Perspective on the M1 Mac mini (A Review)”.</h2>
				</div>
			</div>
		</div>
		<div class="col xl:mt-32 mt-24">
			<div class="xl:flex-row flex-col flex w-full">
				<img class="xl:hidden block home-point-img" src="@/assets/img/script.png" />
				<div class="xl:m-10 mt-8 xl:ml-0">
					<h1 class="home-header-name ml-0-pls mb-2">From script to show.</h1>
					<h2 class="home-point-desc mb-2">
						You want your video done right, the way you imagined it. That’s why I’ll
						make sure that we discuss what you’re looking for, and send you 
						snippets of finished work to gain feedback.
					</h2>
					<h2 class="home-point-footnote">*Note: Finished work snippets are watermarked until the invoice is fully paid.</h2>
				</div>
				<img class="xl:block hidden home-point-img" src="@/assets/img/script.png" />
			</div>
		</div>
		<div class="col xl:mt-32 mt-24">
			<div class="xl:flex-row flex-col flex w-full">
				<img class="home-point-img" src="@/assets/img/captions.png" />
				<div class="xl:m-10 xl:mt-6 mt-8">
					<h1 class="home-header-name ml-0-pls mb-2">Be accessible to all.</h1>
					<h2 class="home-point-desc mb-2">
						If you would like your video to be viewable even by DHH people, you can
						also add on a captioning service, where I will also write captions (with
						formatting of your choice) for your video.
					</h2>
					<h2 class="home-point-footnote">*DHH - Deaf and Hard of Hearing. You may also order the captioning service separately for an already-edited video, even if it was not edited
					by me.</h2>
				</div>
			</div>
		</div>
	</div>
	<div class="home-footer mt-8">
		<div class="home-footer-content col text-center mt-6">
			<h1 class="home-header-name">Let’s get started!</h1>
			<h2 class="home-point-desc mb-4">Would you like to order one of my services? If so, fill out the form below:</h2>

			<h2 class="text-lg text-gray-200 mb-12">If you would prefer to fill out the form on a new page, click <a class="font-medium text-white" target="_blank" rel="noreferrer noopener" href="https://docs.google.com/forms/d/e/1FAIpQLSd3QjK9K24ejWHZldKyootDyCur6jWlZ4ACz7KB-hM8td7aCA/viewform?usp=pp_url&entry.644349022=The+e-mail+address+provided+on+the+form">here</a>.</h2>
			<iframe class="google-form-iframe" frameborder="0" marginheight="0" marginwidth="0" src="https://docs.google.com/forms/d/e/1FAIpQLSd3QjK9K24ejWHZldKyootDyCur6jWlZ4ACz7KB-hM8td7aCA/viewform?embedded=true">Loading...</iframe>
		</div>
		<div class="home-copyright">
			<p>
				All content and this website © 2021 Michael Webb. All rights reserved.
			</p>
			<p class="mt-1 text-gray-200">
				<a class="font-medium" target="_blank" rel="noreferrer noopener" href="https://therandommelon.com">TheRandomMelon Site</a> •
				<a class="font-medium" target="_blank" rel="noreferrer noopener" href="https://youtube.com/TheRandomMelon">YouTube</a> •
				<a class="font-medium" target="_blank" rel="noreferrer noopener" href="https://discord.therandommelon.com">Discord</a>
			</p>
		</div>
	</div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
	components: {
	},
})

export default class Home extends Vue {}
</script>
