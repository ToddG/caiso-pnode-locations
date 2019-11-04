# caiso-pnode-locations

Quick and dirty location information for CAISO PDNODEs.

## Why?

CAISO does not make PNODE location information publicly available. However,
I would like to replicate the Price Map reports as closely as possible:

    http://www.caiso.com/pricemap/Pages/default.aspx

## What?

The PNODES are named, not randomly, but seemingly by the nearby City (or
perhaps nearby county?).  So this project uses various fuzzy match algorithms
comparing the PNODE name to the names of various cities. The output of this
project is a table of PNODEs, a match score, and the matching City and most
importantly, the lat/long of the City.


## How?

* Download city lat/longs from opendatasoft
* Download CAISO network maps with listed PNODES
* Fuzzy match the PDNODEs to the city names
* Generate output file
* Profit!

## Original Data

City Location

* https://public.opendatasoft.com/explore/dataset/us-zip-code-latitude-and-longitude/export/

CAISO Network and Resource Modeling

* http://www.caiso.com/market/Pages/NetworkandResourceModeling/Default.aspx
* http://www.caiso.com/Documents/FullNetworkModel_PricingNodeMapping_Based_FullNetworkModel_ReleaseDB2019Q3.xls
* http://www.caiso.com/Documents/FullNetworkModel_PricingNodeMapping_DB2019Q3withEIM.xls
* www.caiso.com/Documents/FullNetworkModel_PricingNodeMapping_DB2019Q3withEIM.xls

## Links

* http://oasis.caiso.com/mrioasis/logon.do (select Master Control Area Generating Capability List)
* https://www.datacamp.com/community/tutorials/fuzzy-string-python
* https://github.com/jamesturk/jellyfish
* https://pypi.org/project/jellyfish/
* https://www.areavibes.com/ca/
* https://en.wikipedia.org/wiki/List_of_counties_in_California

