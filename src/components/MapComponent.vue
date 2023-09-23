<template>
	<v-container>
		<div id="map"></div>
	</v-container>
</template>

<script>
import L from "leaflet";

export default {
	mounted() {
		// Initialize the map
		var map = L.map("map").setView([51.505, -0.09], 13);

		// Set up the tile layer
		L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
			attribution: "Map data &copy; OpenStreetMap contributors",
		}).addTo(map);
	},
};
</script>

<style>
#map {
	height: 500px;
}
</style>
