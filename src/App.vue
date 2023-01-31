<template>
	<div class="flex flex-col min-h-screen font-Roboto bg-weather-primary">
		<SiteNavigation />
		<!-- v-slot gives us access to information on the route itself such as the component that should be rendered and also the route itself -->
		<RouterView v-slot="{Component}">
			<Transition name="page" mode="out-in">
				<component :is="Component" />
			</Transition>
		</RouterView>
	</div>
</template>

<script setup>
import { RouterView } from 'vue-router';
import SiteNavigation from './components/SiteNavigation.vue';
</script>

<style>
.page-enter-active {
  transition: 600ms ease all;
}
.page-enter-from {
  opacity: 0;
}
</style>