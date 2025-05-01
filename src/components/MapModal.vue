<template>
	<div class="map-modal map">
		<div class="map-header-container">
			<div class="section-header clipped-medium-backward-map">
				<img src="/icons/portrait-icon.svg" />
				<h1>Nov Elysia - Satellite View</h1>
			</div>
			<div class="rhombus-back">&nbsp;</div>
		</div>
		<div class="map">
			<img :src="mapimage" class="map" />
		</div>
	</div>
</template>

<script>
import Markdown from 'vue3-markdown-it';

export default {
	components: {
		Markdown
	},
	props: {
        missionmap: {
			type: Object,
			required: true,
		}
	},
	computed: {
		mapimage() {
            let location = "Nov Elysia"
            let state = ""
			return `/maps/${location}${state}.png`
		},
	},
	created() {

	},
	methods: {

	}
}
</script>