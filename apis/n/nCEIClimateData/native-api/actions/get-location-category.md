# Get Location Category with NCEI Climate Data

Retrieves location category details from NCEI Climate Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/locationcategories/[:locationCategoryId]`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [Get Location Category](https://www.ncei.noaa.gov/cdo-web/webservices/v2#location-categories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationCategoryId` | path | `string` | yes | Location category identifier to retrieve, for example ST or CITY. |
