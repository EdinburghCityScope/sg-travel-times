# sg-travel-times
Edinburgh travel times (minutes) to key services by car or public transport.

Drive times to key services at Data Zone level was originally developed for inclusion in the 2004 Scottish Index of Multiple Deprivation (SIMD), under the Access to Services Domain.

The methodology for generating average drive times to services involves generating drive times for each Census Output Area and then calculating a population weighted average for each Data Zone.

The methodology used to calculate the drive times has changed somewhat over the years, and thus results from different time periods may not be directly comparable. For more detail on current and past methodology please see the report located at http://www.scotland.gov.uk/Topics/Statistics/SIMD/AccessMethodologyPaper.

Automated Teller Machine (ATM, or Cash Machine) locations were included as a key service from 2007, and include street-side locations and machines located within shops or other buildings. Financial Institution locations were included as a key service from 2007, and include banks and building societies. Chemists and Pharmacies were included as a key service from 2007, and include dispensing chemists, drug stores and retail pharmacies. Further Education Establishments were included as a key service from 2007, and include technical schools and colleges. General Stores were included as a key service from 2007, and include outlets such as Londis.

Drive times to GP Surgeries have been included as a service since 2003. Higher Education Establishments were included as a key service from 2007, and include medical schools and universities. Library locations were included as a key service from 2007. Nursery locations were included as a key service from 2007, and include after school care, childcare services, day nurseries, nursery schools, creches, playgroups and pre-school education. Police stations were included as a key service from 2007.

Service locations were obtained from PointX, Ordnance Surveys points of interest dataset, and are geo-referenced by address.

Citizens Advice Bureau locations were included as a key service from 2007. Service locations were obtained directly from Citizens Advice Scotland (CAS), and are geo-referenced by address.

JobCentre Plus locations were included as a key service from 2007. Drive times to Primary Schools have been included as a service since 2003. Drive times to Secondary Schools have been included as a service since 2003. Service locations were obtained directly from the JobCentre Plus Communications Team and are geo-referenced by address.

Drive times to Petrol Stations have been included as a service since 2003. In 2003, service locations were obtained from PointX, Ordnance Surveys points of interest dataset, and are geo-referenced by address. PointX, however, previously relied on Thomson Directories as the source for station locations which relies upon the owners self definition of the service (e.g. some may be defined as a garage rather than a filling station, as that is their main function). For this reason, Catalist data was chosen as the source for station locations for 2006 and later data.

Drive times to Post Offices have been included as a service since 2003. For 2003 and 2006 data, service locations were obtained from PointX, Ordnance Surveys points of interest dataset, and are geo-referenced by address. In 2008, however, the Royal Mail made significant changes to the Post Office network, in terms of closing some conventional branches and in many cases replacing them with outreach services. Location data was obtained directly from Royal Mail, and included information on hours of service. Therefore, for 2009 the data represents those locations which are open for 6 hours or more per week in a fixed location.

Drive times to Retail Centres have been included as a service since 2006, replacing supermarket locations used in 2003. Service locations were derived from CACI Retail Footprint dataset. The retail footprint is a gravity model that defines catchments for shopping centres selling comparison goods in Great Britain. For 2006, locations were derived from a combination of CACI data and Ordnance Surveys PointX dataset, however, for 2009 retail centre information is represented by the CACI information only.


Statistics provided by Scottish Government:  http://statistics.gov.scot/data/travel-times

## License

Data is licensed under the Open Government License: http://www.nationalarchives.gov.uk/doc/open-government-licence/version/2/

## Requirements

- NodeJS
- npm

## Installation

Clone the repository

```
git clone https://github.com/EdinburghCityScope/sg-travel-times.git
```

Install npm dependencies

```
cd sg-travel-times
npm install
```

Run the API (from the sg-travel-times directory)

```
node .
```

Converting the extracted data into loopback data.

```
node scripts/featureCollectionToLoopbackJson.js
```

Re-build data files from the statistics.gov.scot API

```
node scripts/build-data.js
```
