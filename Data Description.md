# Data Description

## New York Location Dataset

The data is freely available and is taken from [NYU Spatial Data Repository](https://geo.nyu.edu/catalog/nyu_2451_34572). The original format of this dataset is a GeoJson file, which is then converted to a CSV. The raw data can be found [here](http://tiny.cc/n82g7y).

The CSV File has the following features:
1. Borough
2. Neighborhood
3. Latitude
4. Longitude

There are a total of 307 records available (including header row) in this dataset. The cleaned dataset is found [here](http://tiny.cc/8s7m7y).  


## Toronto Location Dataset

The dataset of PostalCode, Borough and Neighborhood is scraped from [this](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M) link.
The dataset is then cleaned and merged with the geospatial coordinates of each PostalCode by creating an inner join on 'PostalCode'. The geospatial coordinates of each PostalCode of Toronto could be found [here](http://tiny.cc/od8m7y). 

The [final CSV File](http://tiny.cc/gaan7y) will have the following features:
1. Postal Code
2. Borough
3. Neighborhood
4. Latitude
5. Longitude

The notebook for obtaining the New York City and Toronto data is available [here](http://tiny.cc/a39m7y).  

The above mentioned datasets will be used in conjunction with the [Foursquare API](https://foursquare.com/) for this project. For example, using the Places API of the Foursquare API for different categories like Food, Arts & Entertainment and Nightlife Spot, we would be able to find the frequency of the venues of different categories and the similarities or differences in them for both the cities.
