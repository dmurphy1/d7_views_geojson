# d7_views_geojson
A basic Drupal 7 install with a Views GeoJSON to help serve as a guide during porting the module to D8

To get started:
* Enable views_geojson, geofield, views_ui, views_geojson_content_and_views
* Create a test article with a latitude and longitude
* Naviagte to /locations to view the Views GeoJSON output
* Test a bounding box like /locations?bbox=-72.5,40.1,-69.5,43.9
 * You can use this helper to determine the bounding box: http://harrywood.co.uk/maps/examples/openlayers/bbox-selector.html
 
This project has bowline installed. If Docker is running you can quickly spin up a dev environment. See these tutorials:
* https://github.com/davenuman/bowline
* http://savaslabs.com/2015/04/23/drupal-8-docker-bowline-setup.html
