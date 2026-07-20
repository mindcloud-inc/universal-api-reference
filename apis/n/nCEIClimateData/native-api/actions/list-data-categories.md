# List Data Categories with NCEI Climate Data

Finds data categories in NCEI Climate Data by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/datacategories`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [List Data Categories](https://www.ncei.noaa.gov/cdo-web/webservices/v2#data-categories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetid` | query | `string` | no | Filter data categories by dataset id, such as GSOM. |
| `locationid` | query | `string` | no | Filter data categories by location id. |
| `stationid` | query | `string` | no | Filter data categories by station id. |
