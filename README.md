This project describes a general interface for a
common map component.
It aims to wrap specific implementations like Leaflet
or OpenLayers to enable an easy integration an replacement

In the first step it setup the base for a simple map 
component that displays a tile based map with different
layers and some basic interactions with a hosted application

## Requirements (first draft)
* Display a auto resizeable map in HTML/Angular4 application
* map consists of one tile base layer (for instance OSM)
* the component provides a layer selection dialog
  - map server should be selectable from a list of provided ones
  - map can contain one or more additional layers from GeoJSON or WFS sources
  - map can contain custom dynamic layers with application owned object
  - the visibility of layers in the layer dialog is configurable by hosted application
  - layers can have zoom related visibilities 
  - map can contain multiple clickable layers
* the component can display message boxes for clicked objects
* the component provides a callback interface to inform application about a clicked object
* it is possible to select/deselect objects per API
* the user can select/deselect objects per mouse click or box selection
* the component provides a callback interface to inform application about the selection state of objects
* the component can provide coordinate information about the map
* the component can display additional copyright information 

+ measuring tool
+ grouped objects ( group layers) with custom icons (also weighted group icons)
+ free hand definition of groups / layers
+ Plugin interface for positiong outside fragments on top of the map 
+ Search and index PLUGIn (using the above plugin interface) for searching the maps data interactively. This might also be the reference implementation of the plugin interface

+ Using scs-base for the most bottom data model (out of the box compatibility to some of our present systems). It might only be compatible to the serialized data. Ideally using the formal data model definitions.

## Non Scope
* The component doesn't provide own gis sources
* The component doesn't handle problems related to cross domain access
* Switchable base layer can be implemented later

## Note: Today most of us are using leaflet.js which enables a lot of the requirements out of the box. This should be definietely evaluated to be used as base implementation.
