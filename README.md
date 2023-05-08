# STAC

This repository contains a jupyter notebook with python code for creating a SpatioTemporal Asset Catalog (STAC) <https://github.com/radiantearth/stac-spec>. I am primarily using the package pystac <https://pystac.readthedocs.io/en/stable/>. The python code creates a STAC catalog which consists of nesting json files used to describe geospatial data assets. I am serving the jupyter notebook in Cyverse Discovery Environment and developing the code there. Periodically, I push code changes to this repo. 


Tyson has the STAC API going. I am trying to manually improve the geojson features. I access it by using VSCode. I ssh remote connect to the 'stac-api' virtual machine. 

We currently have it set up to where `collection.json` and `index.geojson` files are located at `/home/ubuntu/cyverse-stac/catalogs`

I am editing the geojson files at `/home/ubuntu/cyverse-stac/catalogs`. 

After I make changes to the geojson, I need to restart the stac-api docker compose. 
```
cd /home/ubuntu/stac-fastapi/
docker-compose restart
```
