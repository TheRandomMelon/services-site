<template>
	<div>
		<nav class="navbar">
			<div class="row flex-shrink-0 h-full" style="width:500px;">
				<router-link class="flex items-center flex-shrink-0 h-full" to="/">
					<img src="@/assets/logo.png" class="nav-logo h-full mr-5 ml-2 mt-1" style="padding: 0.60rem;" />
				</router-link>
				<div class="nav-item-group flex-shrink-0">
					<button id="home" @click="$router.push({name: 'home'})" class="nav-item" active-color="bg-brand-orange">
						<i class="fas fa-home fa-fw"></i> Home
					</button>
					<button id="library" @click="$router.push({name: 'library'})" class="nav-item" active-color="bg-brand-orange">
						<i class="fas fa-book fa-fw"></i> Library
					</button>
					<button id="help" @click="$router.push({name: 'help'})" class="nav-item" active-color="bg-brand-orange">
						<i class="fas fa-question fa-fw"></i> Help
					</button>
					<span @click="console.log('test')" class="nav-indicator"></span>
				</div>
			</div>
			<div style="width:500px;" class="flex-grow">
				<div class="right pr-2">
					<button class="btn bg-primary text-white" @click="$router.push({name:'login'})">Login</button>
				</div>
			</div>
		</nav>

		<!--
		<nav class="nav">
			<button id="e1" @click="handleIndicator('e1')" class="nav-item is-active" active-color="orange">
				<i class="fas fa-home fa-fw"></i> Home
			</button>
			<button id="e2" @click="handleIndicator('e2')" class="nav-item" active-color="orange">
				<i class="fas fa-book fa-fw"></i> Library
			</button>
			<span @click="console.log('test')" class="nav-indicator"></span>
		</nav>
		-->
	</div>
</template>

<script>
	import { Component, Vue, Watch } from 'vue-property-decorator';

	@Component()
	export default class Navbar extends Vue {
		
		items;
		indicator;


		mounted () {
			this.items =  this.$el.querySelectorAll('.nav-item');
			this.indicator = this.$el.querySelector('.nav-indicator');

			this.handleIndicator(this.$route.name);
			//this.items.forEach(item => {if(item.classList.contains('is-active')) this.handleIndicator(item.id)});
		}

		

		@Watch('$route', { deep: true })
		onUrlChange(newVal) {
			this.handleIndicator(newVal.name);
		}


		
		handleIndicator (id) {
			this.items.forEach(item => {
				if(item.id != id) item.classList.remove('is-active');
			});

			if (document.getElementById(id) != undefined) {
				const el = this.$el.querySelector('#' + id);
				this.indicator.style.width = `${el.offsetWidth}px`;
				this.indicator.style.left = `${el.offsetLeft}px`;

				el.classList.add('is-active');
			} else {
				this.indicator.style.width = `0px`;
				this.indicator.style.left = `0px`;
			}
		}
	}
</script>

<style scoped>

	.search-bar {
		width:100%;
		max-width:450px; 
		border-radius: 8px;
		box-shadow: 0px 1px 7px rgba(0, 0, 0, 0.12);
	}

	.right {
		float: right;
	}

	.nav-item-group {
		display: inline-flex;
		position: relative;
		overflow: hidden;
		max-width: 100%;
	}

	

	.nav-item {

		@apply appearance-none;
		@apply outline-none;
		width: 110px;
		text-decoration: none;
		transition: .3s;
		margin: 0 6px;
		z-index: 1;
		font-weight: 500;
		font-size: 15px;
		position: relative;
		
		&:before {
			content: "";
			position: absolute;
			bottom: -6px;
			left: 0;
			width: 100%;
			height: 5px;
			background-color: #dfe2ea;
			border-radius: 0 0 8px 8px;
			opacity: 0;
			transition: .3s;
		}
	}

	.nav-item:not(.is-active):hover:before {
		opacity: 1;
		bottom: 0;
	}

	.nav-indicator {
		position: absolute;
		left: 0;
		bottom: 0;
		height: 4px;
		transition: .4s;
		height: 5px;
		z-index: 1;
		border-radius: 2px 2px 8px 8px;
		box-shadow: 0px 1px 4px -2px rgba(0, 0, 0, 1);
	}

	@media (max-width: 580px) {
		.nav { overflow: auto; }
	}

	.nav-search {
		@apply appearance-none;
		@apply outline-none;
		transition: all 0.3s ease 0s;

		background-color: #FFF;
		flex-basis: 500px;
		font-size: 16px;
		font-family: "Font Awesome 5 Pro", 'Inter', sans-serif;
		@apply py-1;
		letter-spacing: -0.05em !important;
		@apply px-2;
		padding-left: 45px;
		color: rgba(0, 0, 0, 0.5);
	}

	.search-icons i {
		position: absolute;
	}

	.search-icon {
		transition: all 0.3s ease 0s;
		font-size: 17px;
		padding: 7px;
		padding-left: 15px;
		color: rgba(0, 0, 0, 0.18);
	}
	
	.row {
		@apply flex;
		@apply flex-row;
	}

	nav {
		@apply flex;
		@apply top-0;
		@apply inset-x-0;
		@apply items-center;
		z-index:1;
		background: #F9F9F9;
		position: fixed;
		box-shadow: 0px 1px 7px rgba(0, 0, 0, 0.12);
		@apply border-none;
		height: 56px;
	}
</style>
