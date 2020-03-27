<template>
	<ar-container :ar="ar">
		<!--suppress HtmlUnknownTarget -->
		<img :src="src" alt="-" :style="`width:100%;height:100%;object-fit:${fit}`">
	</ar-container>
</template>

<script>
	/**
	 * Props:
	 * 	- src (string, mandatory): the url of the image to be displayed
	 * 	- ar (string, mandatory): the aspect ratio of the image to be displayed: width/height (e.g. 1/1, 4/3, 16/9 etc.)
	 * 	- fit (string, optional): the css image-size (default: cover)
	 */
	
	import ArContainer from 'apl-vue-ar-container';
	
	export default {
		mixins: [],
		
		components: {
			'ar-container': ArContainer,
		},
		
		props: {
			src: String,
			ar: String,
			fit: {
				type: String,
				'default': 'cover',
			}
		},
	}
</script>