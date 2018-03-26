# TigerRide
COSC 412 Term Project 

<!DOCTYPE html>

<html>
    <head>
        <meta name="viewport" content="initial-scale=1.0, user-scalable=no">
        <meta charset="utf-8">
    </head>


    <style>
        #map {
            display: block;
            margin-left: auto;
            margin-right: auto;
            height: 600px;
            width: 50%;
        }
    </style>
    <body>
        <!-- Google Maps API Implementation -->
        <h3>My Google Maps Demo</h3>
        <div id="map"></div>
        <script>

            function initMap() {
                var uluru = {lat: 39.5, lng: -76.4};
                var uluru2 = {lat: 39.4, lng: -76.6};
                var map = new google.maps.Map(document.getElementById('map'), {
                    zoom: 9,
                    center: uluru,
                });
                var marker = new google.maps.Marker({
                    position: uluru,
                    map: map
                });
                var marker2 = new google.maps.Marker({
                    position: uluru2,
                    map: map
                });
            }
        </script>
        <script async defer
                src="https://maps.googleapis.com/maps/api/js?key= AIzaSyCLIg1kqotsvaLVTEVYN0gh_g8a-yW3-E4 &callback=initMap">
        </script>
        <!-- End Google Maps API Implementation -->

        <!-- Code to get lat/long values of current location -->
        <p>Click the button to get your coordinates.</p>

        <button onclick="getLocation()">Try It</button>

        <p id="demo"></p>

            <script>
            var x = document.getElementById("demo");

                function getLocation() {
                    if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition(showPosition);
                    } else {
                x.innerHTML = "Geolocation is not supported by this browser.";
            }
            }

                function showPosition(position) {
                        x.innerHTML = "Latitude: " + position.coords.latitude +
            "<br>Longitude: " + position.coords.longitude;
            }
                function showError(error) {
                    switch (error.code) {
                        case error.PERMISSION_DENIED:
                        x.innerHTML = "User denied the request for Geolocation."
                        break;
                    case error.POSITION_UNAVAILABLE:
                        x.innerHTML = "Location information is unavailable."
                        break;
                    case error.TIMEOUT:
                        x.innerHTML = "The request to get user location timed out."
                        break;
                    case error.UNKNOWN_ERROR:
                        x.innerHTML = "An unknown error occurred."
                        break;
                }
            }

<!-- End code for getting lat/long values -->
    </body>
    
</html>
