This project describes a general interface for a
common map component.
It aims to wrap specific implementations like Leaflet
or OpenLayers to enable an easy integration an replacement

In the first step it setup the base for a simple map 
component that displays a tile based map with different
layers and some basic interactions with a hosted application

## Requirements
### Main
* Display a auto resizeable map in HTML/Angular4 application
* map consists of one tile base layer (for instance OSM)
* the component provides a layer selection dialog
  - ~ ~map server should be selectable from a list of provided ones~ ~
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
* the component provides a callback interface to inform application about the insert and delete of objects
* the component can provide coordinate information about the map
* an application based styling of the component must be possible

### Additional
* the component can display additional copyright information 
+ measuring tool
+ client side grouped objects with API extendable group functions
+ free hand definition of groups / layers (What does that mean? (Eiko))
+ Plugin interface to integrate additional tools 
+ Search and index PLUGIn (using the above plugin interface) for searching the maps data interactively. This might also be the reference implementation of the plugin interface

## Points to research
* How can we handle the localization of component based strings?


## Non Scope
* Authentication also to layer sources is not part of the component
* The component doesn't provide own gis sources
* The component doesn't handle problems related to cross domain access
* Switchable base layer can be implemented later

## Note: 
Today some of us are using leaflet.js which enables a lot of the requirements out of the box. 
It should be a good starting point for a base implementation but one of the goals of the project is
to wrap concrete implementations in a transparent way for the application that uses the component.

## Implementations steps
1. Fix the basic scope and requirements
2. Definition of the basic component interface and the needed basic types
3. Implementation of that basic component
4. Implementation of two different test applications that use the component with different styling
5. Summarize the experiences, solve detected problems
6. ... next steps to extend the component functionality

## Basic component interface
