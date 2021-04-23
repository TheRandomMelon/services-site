<template>
	<div id="main">
		<router-view/>
	</div>
</template>

<script>
import { Options, Vue } from 'vue-class-component';

@Options({
	components: {
	},
})

export default class App extends Vue {}
</script>