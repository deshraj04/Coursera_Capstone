# Data Description

This section describes the data sourced for this project, as well as data cleansing and preparation for subsequent exploration.

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


## Places API of Foursquare

The above mentioned New York City and Toronto datasets will be used in conjunction with the [Foursquare API](https://foursquare.com/) for this project. 

Using the Places API Endpoints of Foursquare for different categories like Food, Arts & Entertainment and Nightlife Spot, we find the frequency of the venues of each of these categories and the similarities or differences in them for both the cities.

### Food Venues by Neighborhood

By using the `explore` API endpoint along with the `categoryId` of the *Food* category we get the nearby venues of the provided location filtered by the *Food* category.

Following is a sample of the data showing the Food venues by a neighbourhood:

	| Neighborhood	| Neighborhood Latitude	| Neighborhood Longitude	| Venue	| Venue Latitude	| Venue Longitude	| Venue Category
  --- :| --- :| --- :| --- :| --- :| --- :| --- :| --- :|
0	|Parkwoods	|43.753259	|-79.329656	|Allwyn's Bakery	|43.759840	|-79.324719	|Caribbean Restaurant
1	|Parkwoods	|43.753259	|-79.329656	|Tim Hortons	|43.760668	|-79.326368	|Café
2	|Parkwoods	|43.753259	|-79.329656	|A&W Canada	|43.760643	|-79.326865	|Fast Food Restaurant
3	|Parkwoods	|43.753259	|-79.329656	|High Street Fish & Chips	|43.745260	|-79.324949	|Fish & Chips Shop
4	|Parkwoods	|43.753259	|-79.329656	|Pizza Pizza	|43.760231	|-79.325666	|Pizza Place


