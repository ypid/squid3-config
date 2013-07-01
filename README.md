# My Squid 3 configuration

This is the configuration that I use to survive the really bad bandwidth of
around 50 kByte/s down link that I get from the "Deutsche Telekom".

# Features
* A lot of fine tuned refresh rules for certain sites to keep those contents
 longer in the cache or to extend the time before the content has to be
 revalidated. This is necessary because a lot of web server administrators do
 not optimize there content for being cached.
* A rewrite Perl script to efficiently cache content which can be accessed
 over different sub domains (this is usually done to handle the load). This is
 used for example by [OpenStreetMap][osm] and [Google Maps][google-maps].
 It is currently implemented using the url_rewrite feature.
 You may want to use [StoreID][] which is being developed for this purpose.

[osm]: http://www.openstreetmap.org/
[google-maps]: http://maps.google.com/
[StoreID]: http://wiki.squid-cache.org/Features/StoreID

# Miscellanies
I also wrote my own configuration for clinets using [Proxy auto-config][PAC] which can be found [here][ypid-PAC].

[PAC]: http://en.wikipedia.org/wiki/Proxy_auto-config
[ypid-PAC]: https://github.com/ypid/scripts/tree/master/WPAD
