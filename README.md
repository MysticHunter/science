<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css">
		<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.0/jquery.min.js"></script>
		<script src="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
		<script src="http://maps.googleapis.com/maps/api/js"></script>
		<script>
			var map;
			function initialize() {
				var mapProp = {
					center:new google.maps.LatLng(-1.2440755,-79.0995695),
					zoom:9,
					mapTypeId:google.maps.MapTypeId.ROADMAP
				};
				map=new google.maps.Map(document.getElementById("googleMap"),mapProp);
			
				$("#mapTab").on('shown.bs.tab', function() {
					// Trigger map resize event so the google map works with bootstrap tabs
					google.maps.event.trigger(map, 'resize');
				});
			}
			
			google.maps.event.addDomListener(window, 'load', initialize);
		</script>
		<style>
			.jumbotron h1 {
				color: black;
				font-size: 35px
			}
			body {
				background-color: cyan;
				color: black;
			}
			.carousel-inner > .item > img,
			.carousel-inner > .item > a > img {
				width: 200px;
				height: 200px;
				margin: auto;
			}
			.myborder {
				border-radius:25px;
				border-style: double;
				background-color: cyan;
			}
		</style>
	</head>
	<body>
		<div class="container">
			<h3></h3>
			<ul class="nav nav-pills">
				<li class="active"><a data-toggle="pill" href="#home">Home</a></li>
				<li><a data-toggle="pill" href="#cycles">cycles</a></li>
				<li><a data-toggle="pill" href="#foodchains">Food chains</a></li>
				<li><a data-toggle="pill" href="#abiotic">Abiotic factors</a></li>
				<li><a data-toggle="pill" href="#limiting">Limiting factors</a></li>
			</ul>
			<div class="tab-content">
				<div id="home" class="tab-pane fade in active">
					<h3>Home</h3>
					<div class="jumbotron">
						<div class="container text-align">
							<center>
								<h1 class="myborder">biosphere 3</h1>
							</center>
						</div>
					</div>
					<div id="myCarousel" class="carousel slide" data-ride="carousel">
						<!-- Indicators -->
						<ol class="carousel-indicators">
							<li data-target="#myCarousel" data-slide-to="0" class="active"></li>
							<li data-target="#myCarousel" data-slide-to="1"></li>
							<li data-target="#myCarousel" data-slide-to="2"></li>
							<li data-target="#myCarousel" data-slide-to="3"></li>
						</ol>
						<!-- Wrapper for slides -->
						<div class="carousel-inner" role="listbox">
							<div class="item active">
								<img src="http://www.breedingpair.com/wp-content/uploads/2009/12/The-Nitrogen-Cycle-300x169.jpg" alt="before explosion" width="50" height="50">
								<div class="carousel-caption">
									<h3>nitrogen cycle</h3>
								</div>
							</div>
							<div class="item">
								<img src="https://c394391.ssl.cf2.rackcdn.com/1431983039.jpg" alt="after explosion" width="50" height="50">
								<div class="carousel-caption">
									<h3>ocean</h3>
								</div>
							</div>
							<div class="item">
								<img src="https://s3.amazonaws.com/engrade-myfiles/4032953163017886/42093carboncycle.png" alt="before explosion" width="50" height="50">
								<div class="carousel-caption">
									<h3>carbon and oxygen cycle</h3>
								</div>
							</div>
							<div class="item">
								<img src="http://s.hswstatic.com/gif/irrigation-photosynthesis.gif" alt="before explosion" width="50" height="50">
								<div class="carousel-caption">
									<h3>photosynthesis cycle</h3>
								</div>
							</div>
							<!-- Left and right controls -->
							<a class="left carousel-control" href="#myCarousel" role="button" data-slide="prev">
							<span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
							<span class="sr-only">Previous</span>
							</a>
							<a class="right carousel-control" href="#myCarousel" role="button" data-slide="next">
							<span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
							<span class="sr-only">Next</span>
							</a>
						</div>
					</div>
				</div>
				<div id="cycles" class="tab-pane fade">
					<h3>Photosynthesis cycle</h3>
					<p>
					the plants in the ecosystem will undergo photosynthesis.  
					The plants will make their own food.  
					They will take in carbon dioxide and breath out oxygen.  
					The fish will take oxygen away from the water and breath out carbon dioxide.
					</p>
					<h3>Nitrogen Cycle</h3>
					<p>
						nitrogen from fish food.
						Ammonia is excreted.
						nitrosomes bacteria convert ammonia to nitrite.
						nitrobacter bacteria convert nitrite to nitrate.
						plants uses nitrates as fertiliser.
						The cycle starts over.
					</p>
					<h3>water cycle</h3>
					<p>
					Water evaporates and goes to the air.
					The water Becomes clouds.
					The clouds release the water making rain.
					The cycle starts over again.
					</p>
					<h3>carbon cycle</h3>
					<p>
						carbon dioxide is released into the air when animls breath, and when fossil fuels are burnt.
						decaying plants carbon dioxide in fossil fuels
						Plants use photosynthesis to decrease the carbon dioxide levels
					</p>
				</div>
				<div id="foodchains" class="tab-pane fade">
					<h3>Food chains</h3>
					<p>
					Fish that would eat the plants.
					Snails that would eat algae and fish waste.
					the plants would make nutrients from sunlight to feed the fish.
					algae will grow and feed the decomposers.
					shrimp would eat algae.
					The algae is produced by sunlight the animals who feed on the algae keep the environment clean.  
					The plants convert fish waste and sunlight into food that will feed the fish.  
					All the organisms work together to create a food web.
					</p>
				</div>
				<div id="limiting" class="tab-pane fade">
					<h3>Limiting factors</h3>
					<ul>
						<li>space</li>
						<li>food source</li>
						<li>predators</li>
						<li>population size</li>
						<li>temperature</li>
					</ul>
				</div>
				<div id="abiotic" class="tab-pane fade">
					<h3>Abiotic factors</h3>
					<ul>
						<li>water depth</li>
						<li>water quality</li>
						<li>humidity</li>
						<li>sand</li>
						<li>air composition</li>
						<li>rocks</li>
						<li>number of hours of sunlight</li>
						<li>strength of the sunlight</li>
						<li>container composition</li>
						<li>air temperature</li>
						<li>water temperature</li>
						<li>size of container</li>
						<li>pH</li>
						<li>soil</li>
						<li>water filtration</li>

					</ul>
				</div>
			</div>
		</div>
	</body>
</html>
