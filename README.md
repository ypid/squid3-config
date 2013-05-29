# My Squid 3 configuration

This is the configuration that I use to survive the really bad bandwidth of
around 50 kByte/s down link that I get from the "Deutsche Telekom".

# Features
* A lot of fine tuned refresh rules for certain sites to keep those contents
 longer in the cache or to extend the time before the content has to be
 revalidated. This is necessary because a lot of web server administrators do
 not optimize there content for being mirrored.
* A rewrite perl script to efficiently mirror content which can be accessed
 over different sub domains (this is usually done to handle the load). This is
 used for example by [OpenStreetMap][osm] and [Google Maps][google-maps].

[osm]: http://www.openstreetmap.org/
[google-maps]: http://maps.google.com/

# Miscellanies
I also wrote my own configuration using [Web Proxy Autodiscovery
Protocol][WPAD] which can be found [here][ypid-wpad].

[WPAD]: http://de.wikipedia.org/wiki/Web_Proxy_Autodiscovery_Protocol
[ypid-wpad]: https://github.com/ypid/scripts/tree/master/WPAD
