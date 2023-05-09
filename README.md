# STAC

This repository contains a jupyter notebook with python code for creating a SpatioTemporal Asset Catalog (STAC) <https://github.com/radiantearth/stac-spec>. I am primarily using the package pystac <https://pystac.readthedocs.io/en/stable/>. The python code creates a STAC catalog which consists of nesting json files used to describe geospatial data assets. I am serving the jupyter notebook in Cyverse Discovery Environment and developing the code there. Periodically, I push code changes to this repo. 


Tyson has the STAC API going. I am trying to manually improve the geojson features. I access it by using VSCode. I ssh remote connect to the 'stac-api' virtual machine. 

We currently have it set up to where `collection.json` and `index.geojson` files are located at `/home/ubuntu/cyverse-stac/catalogs`. You can add new collections by adding a new folder and having 2 files within it: `collection.json` and `index.geojson`. `/home/unbuntu/cyverse-stac/catalogs` is simply holding all of the catalogs. The docker-compose that creates the STAC API is located at `/home/unbuntu/stac-fastapi`.

If you add new catalogs, then you must also add that information to the `home/ubuntu/stac-fastapi/scripts/ingest_cyverse.py`


After I make changes to the `collection.json`, `index.geojson`, or ingest_cyverse.py`, I need to restart the stac-api docker compose. 
```
cd /home/ubuntu/stac-fastapi/
docker-compose restart
```
