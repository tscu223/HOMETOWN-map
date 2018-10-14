# HOMETOWN-map



<head>

	<title>Hometown Map</title>
	<meta name='viewport' content='initial-scale=1,maximum-scale=1,user-scalable=no' />

	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.css" />
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css" />
	<link href="https://fonts.googleapis.com/css?family=Noto+Sans" rel="stylesheet">
	<link href="https://fonts.googleapis.com/css?family=Lora" rel="stylesheet">

	<style>
		body {
			margin: 0;
			padding: 0;
			background: #f5f5f5;
			font-family: "Noto Sans", sans-serif;
			color: #3d3d3d;
		}
		section {
			width: 960px;
			margin: 20px auto;
		}
		h1 {
			font-family: Lora, serif;
			letter-spacing: .04em;
		}
		h2 {
			font-family: Lora, serif;
			letter-spacing: .04em;
		}
		p {
			font-size: 1em;
			line-height: 1.5em;
		}
		a {
			color: #005daa;
			font-weight: bold;
			text-decoration: none;
		}
		a:hover {
			text-decoration: underline;
		}
		ul {
			padding-left: 20px;
		}
		li {
			margin: 10px 0
		}
		#map {
			width: 100%;
			height: 540px;
			margin: 10px auto;
			border: 2px solid #d3d3d3;
		}
		/* This is a comment in CSS styles */
	</style>
</head>

<body>
	<section>

		<!-- This is an HTML comment. Find the comments below and follow the instructions. -->

		<h1>Phoenix, AZ!</h1>

		<div id='map'></div>


		<h2>about this map</h2>
		<p>Additional information about
			<a href="#">the data</a> and map goes here. </p>

		<ul>
			<!-- Change the following contacts to your personal brand, whatever you want it to be! -->
			<li>See my projects on GitHub:<a href="https://github.com/tscu223">Teya's Maps</a>
        </li>


	<script src="https://code.jquery.com/jquery-3.1.1.min.js" integrity="sha256-hVVnYaiADRTO2PzUGmuLJr8BLUSjGIZsDYGmIJLv2b8="
	    crossorigin="anonymous"></script>
	<script src="https://unpkg.com/leaflet@1.3.1/dist/leaflet-src.js"></script>
	<script>
		// This is a comment in JavaScript
		// map options
		var options = {
			center: [33.4484, -112.0740], // lat/lon values
			zoom: 12
		}
		// create a Leaflet map in our division container with id of 'map'
		var map = L.map('map', options);
		// request some basemap tiles and add to the map
		var tiles = L.tileLayer('http://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}.png', {
			attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a> &copy; <a href="http://cartodb.com/attributions">CartoDB</a>',
			subdomains: 'abcd',
			maxZoom: 19
		}).addTo(map);
		// write a custom message for the Leaflet tooltip
		var message = 'Phoenix is Dope!';
		// add a marker to the center of the map and open the tooltip
		L.marker(map.getCenter())
			.bindTooltip(message)
			.addTo(map)
			.openTooltip();
	</script>

</body>

<img src="https://asdb.az.gov/wp-content/uploads/sites/8/2016/10/phoenix-az.jpg" alt="desert">
</html>
