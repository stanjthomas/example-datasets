Fake user data
==============

The "RandumUsers" directory contains files with random users.

    {
      "name": {
	"first": "Diedre",
	"last": "Clinton"
      },
      "gender": "female",
      "birthday": "1959-11-06",
      "contact": {
	"address": {
	  "street": "2 Fraser Ave",
	  "zip": "81223",
	  "city": "Cotopaxi",
	  "state":"CO"
	},
	"email": ["diedre.clinton@nosql-matters.org",
		  "clinton@nosql-matters.org",
		  "diedre@nosql-matters.org"],
	"region": "719",
	"phone": ["719-7055896"]
      },
      "likes": ["swimming"],
      "memberSince":"2009-03-14"
    }

In order to import these users, use:

    ./arangoimp --file names_XXX.json --collection=users --create-collection=true --type=json

where XXX is 100, 1000, 10000, 100000, 200000, 300000.


Cities
======

The Cities directory contains a list of cities with geo
information. There are roughly 320000 cities.

    locId,country,region,city,postalCode,latitude,longitude,metroCode,areaCode
    1,"O1","","","",0.0000,0.0000,,

In order to import these cities, use

    ./arangoimp --file GeoLiteCity.csv --collection=cities --create-collection=true --type=csv


Countries
=========

The Countries directory contains a list of countries with wikipedia
links. There are 241 contries.

    "id","code","name","continent","wikipedia_link","keywords"
    1,"AD","Andorra","EU","http://en.wikipedia.org/wiki/Andorra",

In order to import these countries, use

    ./arangoimp --file countries.csv --collection=countries --create-collection=true --type=csv


Bezirke
=======

The Bezirke directory contains a list of German counties with wikipedia
links. There are 169431 Bezirke.

    RC,UFI,UNI,LAT,LONG,DMS_LAT,DMS_LONG,MGRS,JOG,FC,DSG,PC,CC1,ADM1,POP,ELEV,CC2,NT,LC,SHORT_FORM,GENERIC,SORT_NAME_RO,FULL_NAME_RO,FULL_NAME_ND_RO,SORT_NAME_RG,FULL_NAME_RG,FULL_NAME_ND_RG,NOTE,MODIFY_DATE
    1,6132652,6143433,52.5,13.283333,523000,131700,33UUU8347218037,NN33-10,A,ADM2,,GM,16,,,,N,,Charlottenburg-Wilmersdorf,Bezirk,BEZIRKCHARLOTTENBURGWILMERSDORF,Bezirk Charlottenburg-Wilmersdorf,Bezirk Charlottenburg-Wilmersdorf,CHARLOTTENBURGWILMERSDORF BEZIRK,"Charlottenburg-Wilmersdorf, Bezirk","Charlottenburg-Wilmersdorf, Bezirk",,2001-12-20

In order to import these counties, use

    ./arangoimp --file bezirke.csv --collection=bezirke --create-collection=true --type=csv


Airports
========

The Airports directory contains a list of airports with geo
information. There are roughly 44000 airports.

    "id","ident","type","name","latitude_deg","longitude_deg","elevation_ft","continent","iso_country","iso_region","municipality","scheduled_service","gps_code","iata_code","local_code","home_link","wikipedia_link","keywords"
    6523,"00A","heliport","Total Rf Heliport",40.07080078125,-74.9336013793945,11,"NA","US","US-PA","Bensalem","no","00A",,"00A",,,

In order to import these airports, use

    ./arangoimp --file airports.csv --collection=airports --create-collection=true --type=csv


IP Address Ranges
=================

The IPRanges directory contains IP address ranges and geo
information. There are 3.7 Million ranges.

    {
      "locId" : "17",
      "endIpNum" : "16777471",
      "startIpNum" : "16777216", 
      "geo" : [ -27, 133 ] 
    }

In order to import these locations, use:

    ./arangoimp --file geoblocks.json --collection=ip_ranges --create-collection=true --type=json
