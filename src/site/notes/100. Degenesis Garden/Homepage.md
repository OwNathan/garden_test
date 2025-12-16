---
{"dg-publish":true,"permalink":"/100-degenesis-garden/homepage/","tags":["gardenEntry"]}
---


<link rel="stylesheet" href="[https://unpkg.com/leaflet@1.7.1/dist/leaflet.css](https://unpkg.com/leaflet@1.7.1/dist/leaflet.css)" />
<script src="[https://unpkg.com/leaflet@1.7.1/dist/leaflet.js](https://unpkg.com/leaflet@1.7.1/dist/leaflet.js)"></script>
<div id="map" style="height: 500px; width: 100%;"></div>
<script>
  var map = L.map('map', {
    crs: L.CRS.Simple, // This tells Leaflet it's a flat image, not a world map
    minZoom: -1,
    maxZoom: 2
  });
  var w = 2116; // CHANGE THIS to your image width
  var h = 1788; // CHANGE THIS to your image height
  var bounds = [[0, 0], [h, w\|0, 0], [h, w]];
  var image = L.imageOverlay('https://raw.githubusercontent.com/OwNathan/garden_test/refs/heads/main/degenesis-rebirth-world-map-en-3264x2320.png', bounds).addTo(map);
  map.fitBounds(bounds);
  L.marker([h/2, w/2]).addTo(map)
    .bindPopup("<b>Welcome!</b><br>This is the center of the map.");
</script>