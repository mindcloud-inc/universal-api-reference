# Get Data Category with NCEI Climate Data

Retrieves data category details from NCEI Climate Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/datacategories/[:dataCategoryId]`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [Get Data Category](https://www.ncei.noaa.gov/cdo-web/webservices/v2#data-categories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataCategoryId` | path | `string` | yes | Data category identifier to retrieve, for example TEMP. |
