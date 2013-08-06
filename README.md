RTA API API
===

RTA transit data from next bus, for those who don't care for XML.

Install with:
```
npm install rta
```

commands

```javascript
var RTA = require('rta');
var rta = new RTA(agency tag, seconds to cache(default is 10));
rta.locations(route[,since,cb]);
	->geojson from the bus GPS
rta.stop(stop[,cb]);
	->predictions for a stop
rta.list([cb]);
	->list of route IDs
rta.route(route[,cb]);
	->information about a route
rta.schedule(route[,cb]);
	-> schedule of the route.
```

It returns a promise so you can omit the callback if you're into that.

Not affiliated with the Next bus or any transit company. Inspired by [Tom MacWright](https://github.com/tmcw)'s [wmataapiapi](https://github.com/tmcw/wmataapiapi).
