# Lotería Electrónica de Puerto Rico - Mapa: ¿Dónde Jugar?

An attempt to obtain the dataset used for the _"Lotería Electrónica de Puerto Rico - ¿Dónde Jugar?"_ map.

## Map

Google Map containing `FusionTablesLayer` with coordinates.

**URL:** http://www.loteriaelectronicapr.com/mapa.htm

> Contained as `<iframe>` inside:  
> http://www.loteriaelectronicapr.com/dondejugar

## Map Layer

Google maps `FusionTablesLayer` defined as:

```javascript
layer_1 = new google.maps.FusionTablesLayer({
            query: {
                select: 'col3',
                from: '4935531'
            },
            map: map,
            suppressInfoWindows: true
        });

```

## Fusion Table

Reading the Fusion Tables documentation, the `fusionTableID` used in the `from:` definition uses the **old (deprecated)** numeric ID.

> **Important! Deprecating numeric table IDs: **  
> https://groups.google.com/forum/#!msg/fusion-tables-api-announce/_KI_HnWT9V4/S-ZeAYC2zkoJ  
> _Source: [Fusion Tables API Announce (Google Groups)](https://groups.google.com/forum/#!forum/fusion-tables-api-announce)_

**Fusion Table document can be accessed using the following URLs:**

* **Using old numeric ID:**  
  https://www.google.com/fusiontables/data?dsrcid=4935531
* **Using new document ID:**  
  https://www.google.com/fusiontables/data?docid=1vQydIHO1RNzqocLwdsZ_MyJZjeoZv_VmY5u9aQw

## ¿Dónde Jugar?

> Imported at Sat Aug 18 16:23:10 PDT 2012 from `LE_DondeJugar.xls`.  
> Last updated on September 5, 2013.  

#### Data Fields

* `name` - Establishment Name
* `phone` - Phone Number
* `latitude2` - Latitude
* `longitude2` - Longitude
* `addd` - Establishment Address

#### Data Formats

* **CSV**  
    * [LE_DondeJugar.csv](LE_DondeJugar.csv) [[Source](https://www.google.com/fusiontables/exporttable?query=select+*+from+1vQydIHO1RNzqocLwdsZ_MyJZjeoZv_VmY5u9aQw&o=csv)]
* **KML**  
    * [LE_DondeJugar.kml](LE_DondeJugar.kml) [[Source](https://www.google.com/fusiontables/exporttable?query=select+col2+from+1vQydIHO1RNzqocLwdsZ_MyJZjeoZv_VmY5u9aQw&o=kml&g=col2&styleId=7&templateId=2)]
* **GeoJSON**
    * [LE_DondeJugar.geojson](LE_DondeJugar.geojson) (Converted using [toGeoJSON](http://mapbox.github.io/togeojson/) tool)
