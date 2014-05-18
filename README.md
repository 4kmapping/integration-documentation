# 4k integration documentation

This repository aims to be a collection of documentation with examples on how to integrate your project with the 4k framework. Please feel free to add ways to integrate that aren't in this list.

The ArcGIS Online Map Service the Omega Zones are currently hosted is at `https://services1.arcgis.com/DnZ5orhsUGGdUZ3h/ArcGIS/rest/services/OZ2014/FeatureServer/0`.
This is the 2014 version of the Omega Zones.

## Examples

The following integration examples are currently available;

- **Showing Omega Zones on a simple map** *(map-with-omega-zones.html)*
	- Shows how to throw Omega Zones on top of an interactive map.
	- Has horrible performance (zoom out to world level)
		- Check out the [oz-perf-tests](https://github.com/joshuadelange/oz-perf-tests) repository for experiments to try to optimize performance.
	- For more information, check out ESRI's JS API;
		- [Creating a map](https://developers.arcgis.com/javascript/jssamples/map_simple.html)
		- [FeatureLayer](https://developers.arcgis.com/javascript/jsapi/featurelayer-amd.html)
- **World ID lookups**
	-  **By Map Point** *world-id-lookup-point.html*
	-  **By Lat + Lon** *world-id-lookup-lat-lon.html*
	- Important ESRI API components;
		- [QueryTask](https://developers.arcgis.com/javascript/jsapi/querytask-amd.html)
			- Specifies the Omega Zone map service to check against
			)
		- [Query](https://developers.arcgis.com/javascript/jsapi/query-amd.html)
			- The actual query
			- This is where you can specify what fields you want
				- Check out [the service](https://services1.arcgis.com/DnZ5orhsUGGdUZ3h/ArcGIS/rest/services/OZ2014/FeatureServer/0) for a complete list of fields you can select