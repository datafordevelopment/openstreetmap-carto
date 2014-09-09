# OpenStreetMap Carto

![screenshot](https://raw.github.com/gravitystorm/openstreetmap-carto/master/preview.png)

These are the CartoCSS map stylesheets for the Standard map layer on [OpenStreetMap.org](http://www.openstreetmap.org).

These stylesheets can be used in your own cartography projects, and are designed to be easily
customised. They work with [TileMill](http://www.mapbox.com/tilemill/) and also with the command-line [CartoCSS](https://github.com/mapbox/carto) processor.

Since August 2013 these stylesheets have been used on the OSMF tileservers (tile.openstreetmap.org), and
are updated from each point release. They supersede the previous [XML-based stylesheets](https://trac.openstreetmap.org/browser/subversion/applications/rendering/mapnik)

# Installation

You need a PostGIS database populated with OpenStreetMap data in the standard
osm2pgsql database layout, along with auxillary shapefiles. See [INSTALL.md](INSTALL.md)

# Contributing

Contributions to this project are welcome, see [CONTRIBUTING.md](CONTRIBUTING.md)
for full details

# Roadmap

## Initial Release (v1.0.0, December 2012)

This was a full re-implementation of the original OSM style, with only a few bugs discovered later. There's been
no interest in creating further point releases in the v1.x series.

## Current work (v2.x)

The v2.x series focuses on refactoring the style, both to to fix glitches and to
leverage new features in CartoCSS / mapnik to simplify the stylesheets with only
small changes to the output. It's also appropriate to pull out the 'old-skool'
tagging methods that are now rarely used.

Care is being taken to not get too clever with variables and expressions. While these often make
it easier to customise, experience has shown that over-cleverness (e.g. [interpolated entities][cleverness])
can discourage contributions.

The end goal will be a style that remains familiar but is much more suitable for
further development, and/or forking for third-parties to customise.

## Future (v3.x)

There are over [300 open requests][issues], some that have been open for years. These need
reviewing and dividing into obvious fixes, or additional new features that need some cartographic
judgement. The work done already in v1.0 and v2.0 will make it much easier to process these.

[issues]: https://github.com/gravitystorm/openstreetmap-carto/issues
[cleverness]: https://github.com/openstreetmap/mapnik-stylesheets/blob/master/inc/settings.xml.inc.template#L16

# Maintainers

* Andy Allan [@gravitystorm](https://github.com/gravitystorm/)
* Matthijs Melissen [@math1985](https://github.com/math1985/)
* Paul Norman [@pnorman](https://github.com/pnorman/)
* Mateusz Konieczny [@mkoniecz](https://github.com/mkoniecz/)
