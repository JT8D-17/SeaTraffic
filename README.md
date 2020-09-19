# SeaTraffic plugin for X-Plane<sup>®</sup> 11.50+

&nbsp;

SeaTraffic is an [X-Plane](x-plane.com) plugin that displays ships moving along real-life routes.   

This repository contains a complete plugin distribution for **the Linux version of X-Plane 11.50+** (including some ship models) as well as the source code for the X-Plane plugin.   
User oriented documention is contained in the file SeaTraffic-ReadMe.html.
&nbsp;

## Requirements

- Linux (an up-to-date distro)
- [X-Plane 11](https://www.x-plane.com/) (11.50 or higher)
- [OpenSceneryX](https://www.opensceneryx.com/)
- Python 3.x (for building/updating the routes list)

&nbsp;

## Installation

Copy the "SeaTraffic" folder into

	X-Plane 11/Resources/Plugins
	
&nbsp;


## (Re)Building the plugin

To clean a previous build from the _"build"_ and _"SeaTraffic/64"_ subfolders (if present):
	
	make clean
	
To compile a new _lin.xpl_ file, output in _"build"_
	
	make
	
To move _lin.xpl_ from the _"build"_ subfolder to the _"SeaTraffic/64"_ subfolder
	
	make install

&nbsp;	

## Building the routes list

The routes list is built from the `SeaTraffic` directory, and requires Python 3.x.

    buildroutes.py
    
&nbsp;

## About this plugin fork

- Based on nst0022's commit as of [18/09/2020](https://github.com/nst0022/SeaTraffic/commit/c7f4129369963933daf4276016d384fa214a5429).
- New makefile for 64bit Linux only
- Includes prebuilt 64bit lin.xpl file in plugin folder
- Includes X-Plane SDK folder
- Gave nst0022 some credit in the plugin description


&nbsp;

##Known issues / Help required

- No Windows build ; requires external input
- No MacOS build ; requires external input
- Reflection slider does not have any effect on wakes ; requires investigation
- Assert messages need to be piped through the XPLMDebugMessage system to be viewable outside of the terminal ; requires rewite