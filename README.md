# d7_views_geojson
A basic Drupal 7 install with a Views GeoJSON to help serve as a guide during porting the module to D8

To get started:
* Enable views_geojson, geofield, views_ui, views_geojson_content_and_views
* Create a test article with a latitude and longitude
* Naviagte to /locations to view the Views GeoJSON output
* Test a bounding box like /locations?bbox=-72.5,40.1,-69.5,43.9
 * You can use this helper to determine the bounding box: http://harrywood.co.uk/maps/examples/openlayers/bbox-selector.html
 
This project has bowline installed, meaning you can quickly spin up a dev environment by doing the following:
* Make sure docker is running. On a Mac with Boot2Docker that means running the following:
 * `boot2docker start`
 * `eval "$(boot2docker shellinit)"`
 * `sudo route -n add 172.0.0.0/8 192.168.59.103`
* Activate bowline:
 * `. bin/activate`
 * `build`
* Setup the site:
 * `settings_init`
 * `drush si --sites-subdir=default`
 * `drush views_geojson, geofield, views_ui, views_geojson_content_and_views`
 * Run `bowline` to get the site IP address.
* Test it out:
 * Create a test article with location at `/node/add/article`
 * Visit `/locations` to see the Views GeoJSON Output

See these bowline installation instructions for more detail:
* https://github.com/davenuman/bowline
* http://savaslabs.com/2015/04/23/drupal-8-docker-bowline-setup.html
