titanium-location-module
========================

This module is a drop-in wrapper for the Titanium GPS functionality.  
It was extracted from a titanium app used to collect surveys on the field. [Link](https://github.com/c42/survey-mobile)    
We built this module because the location provided by the Titanium API is inaccurate in most cases.
We tried a lot of approaches that didn't work before we arrived at this one. We hope this helps.

Usage
-----

```javascript
var location = require('path/to/location/js');
location.start({
	action: function(responseLocation) {
		// Do something after getting location.
	},
	error: function() {
		// Do something if not able to get location after 25 seconds
	}
});
```

After the `action` callback is called, Location.js will keep trying to get a better location in the background.  
You need to call `location.stop()` explictly when you're satisfied with the location.

Contributors
--------
* Nivedita Priyadarshini
* Smit Shah
* Timothy Andrew
