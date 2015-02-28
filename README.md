# My Squid 3 configuration
This is the configuration that I used to survive the really bad bandwidth of
around 50 kByte/s down link that I got from the "Deutsche Telekom".

# Features
* A lot of fine tuned [refresh rules][refresh-pattern] for certain sites to
 keep those contents longer in the cache or to extend the time before the content has to be
 revalidated. This is necessary because a lot of web server administrators do
 not optimize there content for being cached.
* More refresh rules that are based on file suffixes and assumptions about the
 modification frequency of those files. There are some directives used that
 **violate HTTP!** Mainly because explicit reloads form clients are ignored for
 some files and the requests are directly satisfied from the cache without
 revalidation! I find it more acceptable to see a slightly out-dated version of
 some files than waiting too long.
* A rewrite Perl script to efficiently cache content which can be accessed
 over different sub domains (this is usually done for load balancing). This is
 used for example by [OpenStreetMap][osm] and [Google Maps][google-maps].  It
 is currently implemented using the url_rewrite feature.  You may want to use
 [StoreID][] which is being developed for this purpose.

[osm]: http://www.openstreetmap.org/
[google-maps]: http://maps.google.com/
[refresh-pattern]: http://www.squid-cache.org/Doc/config/refresh_pattern/
[StoreID]: http://wiki.squid-cache.org/Features/StoreID

# Miscellanies
I also wrote my own configuration for clients using [Proxy auto-config][PAC]
which can be found [here][ypid-PAC].

[PAC]: http://en.wikipedia.org/wiki/Proxy_auto-config
[ypid-PAC]: https://github.com/ypid/scripts/tree/master/WPAD
