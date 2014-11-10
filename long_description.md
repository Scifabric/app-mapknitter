MapKnitter is a <strong>demo application</strong> for PyBossa that shows how you can 
crowdsourcing a geo localization problem with <a href="http://mapknitter.org">MapKnitter</a> as the backend.

This application uses a map from MapKnitter where there are several camp tents. The 
goal is really simple: navigate the map in order to count the number of tents by adding a point or polygon on top of each tent.

When the user adds a polygon or a point, the action saves the position and
the coordinates in GeoJSON format to easily parse it at a later stage.


**Note** If you want to learn more about how to use this application as a
template, check the:

 * [source code](http://github.com/PyBossa/app-geocoding)
 * [documentation](http://docs.pybossa.com), and
 * [the step by step tutorial](http://docs.pybossa.com/en/latest/user/tutorial.html)
