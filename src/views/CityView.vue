<template>
	<div>
		<!-- Component <Anonymous>: setup function returned a promise, but no <Suspense> boundary was found in the parent component tree. A component with async setup() must be nested in a <Suspense> in order to be rendered.  -->
		<Suspense>
			<AsyncCityView />
			<template #fallback>
				<CityViewSkeleton />
			</template>
		</Suspense>
	</div>
</template>

<script setup>
import AsyncCityView from '../components/AsyncCityView.vue';
import CityViewSkeleton from '../components/CityViewSkeleton.vue';

</script>