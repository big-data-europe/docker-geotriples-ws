# docker-geotriples-ws

Geotriples is a tool for publishing geospatial data as Linked Open Geospatial Data. You can find more informatin here: https://github.com/LinkedEOData/GeoTriples.

Geotriples is used as service for the BDE SC7 pilot.

Example usage

Run the docker:
$ docker run  -p 9999:8080 gioargyr/geotriples-ws:2.3.0

Trigger it through command line:
$ curl -X POST -d @<filepath_to>/post_geo.json http://localhost:9999/geotriples/event -H "Content-Type:application/json" -H "Accept: application/json"
or
$ curl -X POST -d @<filepath_to>/changes.json http://localhost:9999/geotriples/changes -H "Content-Type:application/json" -H "Accept: application/json"

After it is triggered it will search for strabon @ localhost:8193 to save the triples.

The testing files post_geo.json and changes.json are in file testing-files of this repo.
