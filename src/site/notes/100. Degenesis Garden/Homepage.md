---
{"dg-publish":true,"permalink":"/100-degenesis-garden/homepage/","tags":["gardenEntry"]}
---


<link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
<div id="map" style="height: 500px; width: 100%;"></div>
<script>
  var map = L.map('map', {
    crs: L.CRS.Simple,
    minZoom: -2,  // Allowed zooming out further to see the whole map
    maxZoom: 2
  });
  // 2. CORRECT DIMENSIONS (Matches your filename: 3264x2320)
  var w = 2116; // CHANGE THIS to your image width
  var h = 1788; // CHANGE THIS to your image heigh
  var bounds = [[0, 0], [h, w\|0, 0], [h, w]];
  // 3. CORRECT URL (Removed 'refs/heads/')
  var url = 'https://raw.githubusercontent.com/OwNathan/garden_test/main/degenesis-rebirth-world-map-en-3264x2320.png';

  var image = L.imageOverlay(url, bounds).addTo(map);
  map.fitBounds(bounds);
  L.marker([h/2, w/2]).addTo(map)
    .bindPopup("<b>Welcome to Degenesis!</b><br>Center of the World.");
</script>
