# rC3-OSM-Map

This repo contains some maps built with the [Tiled Map Editor](https://www.mapeditor.org/) which might be used for the [OSM assembly](https://wiki.openstreetmap.org/wiki/Chaos_Communication_Congress/rC3) in the [WorkAdventure](https://workadventu.re/)-based world at [rC3](https://rc3.world/). See the [rC3 world maps howto](https://howto.rc3.world/maps.html) and the [official WorkAdventure documentation](https://workadventu.re/map-building/) about how to build maps.

## Map development

This repository also contains a simple, Python3 based web server in `serve-maps.py` which uses [`http.server`](https://docs.python.org/3/library/http.server.html) to serve the content of this repository:

	python3 serve-maps.py

By default, this starts a [local web server on port 8000](http://localhost:8000) which serves the [`index.html`](index.html) file and the maps. [`index.html`](index.html) contains a hard-coded list of maps in this repository which gets turned into a list of links to the public WorkAdventure instance using the local URLs of the maps, so they can be viewed in the browser by following the links.

## Maps

- [rC3-OSM-Tileset Example](osm-example.json) - Map which uses various tiles from the [rC3-OSM-Tileset](https://github.com/mstock/rC3-OSM-Tileset) and several of the [WorkAdventure](https://workadventu.re/) features.
- [Main](main.json) - Main map which may serve as an entry point in the [rC3 world](https://rc3.world/).

## Used Tilesets

Please note that the tilesets are included as [Git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules), so you will have to `git submodule update --init --recursive` them before they are available.

* [rC3-OSM-Tileset](https://github.com/mstock/rC3-OSM-Tileset): Tileset based on the [OpenStreetMap Carto](https://github.com/gravitystorm/openstreetmap-carto) map style.
* [world-tiles](https://git.cccv.de/rc3/world-tiles): Shared tilesets for the rC3 world. Please note that these tilesets may be provided under a different license than the remainder of this repository, but they should all be usable for the purpose of building a map for the [rC3 world](https://rc3.world/).

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)
