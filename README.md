PyBossa MapKnitter application
==============================

This demo application shows how you can analyze a [MapKnitter](http://mapknitter.org/) 
map in a PyBossa server like CrowdCrafting.org.

The application is a simple demo that uses OpenLayers JavaScript library to load a map,
center it and add one or more points/polygons to the map. 


This demo is using the map created by [mlamadrid](http://mapknitter.org/map/view/juakali).
The map shows a Craft Village in Nsambya, Kampala and the goal of this demo is
to show that after creating the map in MapKnitter, you can analyze it very
easily. For example, this demo application allows you to count the number of
tents, or even measure its size drawing polygons on top of them. 

Thanks to the use of OpenLayers the data can be exported in any standard GIS format:
KML, GeoJSON, etc. In this application the answers are saved as GeoJSON.

![alt screenshot](http://i.imgur.com/kTgUEL0.png)

The application has three files:

*  createTasks.py: for creating the application in PyBossa
*  template.html: the view for every task and deal with the data of the answers.
*  tutorial.html: a simple tutorial for the volunteers.

Testing the application:
=======================
You need to install the pybossa-client and the soundcloud client (use a virtualenv):

```bash
    $ pip install -r requirements.txt
```

*  Create an account in PyBossa
*  Copy under your account your API-KEY
*  Run python createTasks.py -u http://crowdcrafting.org -k API-KEY
*  Open with your browser the *Applications section* and choose the MapKnitter
   application. This will open the presenter for this demo application.


Using your own MapKnitter map
=============================

In order to use your own MapKnitter map, you will need the URL of the TMS layer
provided by MapKnitter, and split it into two different parts. For example, if
the URL of the TMS layer is: http://mapknitter.org/tms/NAME/

You will have to copy the NAME and paste it in the variable **layername**, in
the section MapKnitter TMS Layer


Then, check for the coordinates of the center of your map, add them to a file
called coordinates (Lon,Lat) one pair per line, and you will be done. This is
useful if you want to analyze different areas of your map. Each area will
become a PyBossa task.


Documentation
=============

We recommend that you read the section: [Build with PyBossa](http://docs.pybossa.com/en/latest/build_with_pybossa.html) and follow the [step by step tutorial](http://docs.pybossa.com/en/latest/user/tutorial.html).

**NOTE**: This application uses the [pybossa-client](https://pypi.python.org/pypi/pybossa-client) in order to simplify the development of the application and its usage. Check the [documentation](http://pythonhosted.org/pybossa-client/).

LICENSE
=======

Please, see the COPYING file.

Acknowledgments
===============
The thumbnail has been created using a [photo](http://www.flickr.com/photos/bulle_de/4672972586/) from Christopher Bulle (license CC¬BY 2.0).
