<template>
	<div class="page index">
		<container>
			<h1 class="text-grey-700 text-3xl">
				Accueil
			</h1>
		</container>
	</div>
</template>

<style lang="stylus" scoped>
	.page.index {

	}
</style>

<script>
import { TimelineLite } from 'gsap'

export default {
	mounted() {
		console.log({ page: this.$route.name })
	},
	head() {
		return {
			title: 'Nuxt Boilerplate | Accueil',
			meta: [
				{ hid: 'description', name: 'description', content: 'This is the homepage' },
			]
		}
	},
	transition: {
		mode: 'out-in',
		css: false,
		appear: true,
		enter (el, done) {
			let tl = new TimelineLite({ onComplete: done })

			tl.add('start')
		},
		leave (el, done) {
			let tl = new TimelineLite({ onComplete: done })

			tl.add('start')
		}
	}
}
</script>

