<template>
	<div class="page {{ dashCase name }}">
		<container>
			<h1>
				<!-- content -->
			</h1>
		</container>
	</div>
</template>

<style lang="stylus" scoped>
.page.{{ dashCase name }} {

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
			title: 'Nuxt Boilerplate | {{ titleCase name }}',
			meta: [
				{ hid: 'description', name: 'description', content: 'This is a new page' },
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
