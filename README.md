Cordova GoogleMaps plugin for iOS and Android
==========================
This plugin is a thin wrapper for [Google Maps Android SDK v2](https://developers.google.com/maps/documentation/android/) and [Google Maps SDK for iOS](https://developers.google.com/maps/documentation/ios/).
Both [PhoneGap](http://phonegap.com/) and [Apache Cordova](http://cordova.apache.org/) are supported.

-----

###Some info

I forked this repo form the v1.4.0 & added styles support in both Android & iOS platforms. Clustering works with both platforms now, but still has some bugs on iOs devices while it's working fine with Android. Here's a code example on how to use it:

```javascript
this.mapParams = {
			'styles' : require("../../data/mapStyle.json"),
			'camera': {
				'latLng': this.defaultPosition,
				'zoom': 7
			},
			'controller': {
				'clustering': true,
				'rendering': 'animated',
				'algorithm': 'nonHierarchicalDistanceBasedAlgorithm'
			}
		};
  this.map = plugin.google.maps.Map.getMap(this.el, this.mapParams);
```
