# Overview

Web page to get the user's location, either automatically or manually, and
provide a page that can be given to other people that links to popular map
services for that location. When the [Web Share API](https://w3c.github.io/web-share/)
is supported the location page can be shared (also available directly from
the "current location" view).

Examples:
* [start page](https://maps.uuid.uk/)
* [the White House](https://maps.uuid.uk/#38.897778,-77.036389)

Inspired by [find.me.uk](https://find.me.uk/) and [GeoHack](https://www.mediawiki.org/wiki/GeoHack).

Copyright and trademark information for the image files is located inside
the [web page](index.htm) and I'm not going to repeat it here.

# Design/requirements

On a portrait mobile phone, this web page must look good and fit all the
services in without scrolling.

The page must be usable and load quickly even on slow data connections
(images must have alt text and fixed sizes so that they can be used before
loading completes).

Web page map links should open with:
* A "dropped pin" on the exact location (not the nearest feature)
* Maximum zoom level (by default)
* Interface to quickly get directions to the location
* The co-ordinates as the name of the location (if possible)
* Default layer (not satellite)

Getting and refreshing the current location must be automated and display
useful status information.

Location information must never be transmitted to the web server hosting the web
page. Location information must not be transmitted to any other service except
by providing manually activated links containing that information to the user.
