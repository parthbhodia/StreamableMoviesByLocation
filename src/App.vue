<template>
	<div id="app">
		<!-- <SearchBarComponent @search="performSearch" /> -->
		<!-- <FiltersComponent @filter="applyFilters" /> -->
		<MapComponent :movies="filteredMovies" />
	</div>
</template>

<script>
// import SearchBarComponent from "./components/SearchBarComponent.vue";
// import FiltersComponent from "./components/FiltersComponent.vue";
import MapComponent from "./components/MapComponent.vue";
import moviesData from "./assets/moviesData.json";

export default {
	components: {
		// SearchBarComponent,
		// FiltersComponent,
		MapComponent,
	},
	data() {
		return {
			movies: moviesData,
			filteredMovies: moviesData,
			searchQuery: "",
			filters: {},
		};
	},
	methods: {
		performSearch(query) {
			this.searchQuery = query;
			this.updateFilteredMovies();
		},
		applyFilters(filters) {
			this.filters = filters;
			this.updateFilteredMovies();
		},
		updateFilteredMovies() {
			// Your logic here to filter movies based on searchQuery and filters
		},
	},
};
</script>

<style>
/* Add your global styles here */
</style>
