# Opentender Portal Data Folder

Data files for all Opentender Apps

Separated from the apps so apps can by started by a user with read-only access (except this folder)

```
├── backend 
│   ├── mappings_NUTS-2013
│   ├── pc2016_NUTS-2013
│   └── stop-words
├── shared
│   └── downloads
│   └── nuts
│   └── country-names
└── tenderapi // used by backend and scrape app
    └── import
```

## backend

used by backend app only

```
├── cpvs.json // list of cpv codes, names and translations (https://simap.ted.europa.eu/cpv)
├── mappings_NUTS-2013 // mappings from older/newer NUTS version to 2013 version
│   ├── mapping_de_NUTS-2013.json
│   ├── mapping_fi_NUTS-2013.json
│   ├── mapping_fr_NUTS-2013.json
│   …
├── pc2016_NUTS-2013 // mapping postcode => NUTS2013  (http://ec.europa.eu/eurostat/tercet/download.do?file=pc2016_NUTS-2013.zip)
│   ├── README
│   ├── pc2016_at_NUTS-2013_v2.3.json
│   ├── pc2016_be_NUTS-2013_v2.3.json
│   ├── pc2016_bg_NUTS-2013_v2.3.json
│   …
├── cpv // mapping older/other cpv codes, cpv names
│   ├── README
│   ├── cpvs_2008.json // names of CPVS
│   ├── mapppings_cpvs_2003_2007.csv 
│   …
└── stopwords.txt // combined stopwords file for elastic search analyzer fields (https://github.com/Alir3z4/stop-words)
```

## shared

used by backend and frontend app

```
├── portals.json // list of all active & inactive portals and their meta data, e.g. country specific FOI portal informations 
│── schema.json // Opentender Data Format Definition
│── tenderapi.json // TenderApi Data Format Definition
└── country-names // Country names in several languages
    ├── bg.json
    ├── cs.json
    ├── da.json
    …
└── nuts // nuts shapes as geojson for use in maps
    ├── nuts_20M_lvl0.geo.json
    ├── nuts_20M_lvl1.geo.json
    ├── nuts_20M_lvl2.geo.json
    …
└── downloads // place where generated country specific user downloads are stored (empty in repository)
    ├── data-am.ndjson.gz
    ├── data-at.ndjson.gz
    …
    └── downloads.json
```

## tenderapi 

Datasets are here
