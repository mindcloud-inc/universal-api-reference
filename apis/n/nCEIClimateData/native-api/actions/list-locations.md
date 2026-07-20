# List Locations with NCEI Climate Data

Finds locations in NCEI Climate Data by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [List Locations](https://www.ncei.noaa.gov/cdo-web/webservices/v2#locations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datacategoryid` | query | `string` | no | Filter locations by data category id, such as TEMP. |
| `datasetid` | query | `string` | no | Filter locations by dataset id, such as GHCND. |
| `locationcategoryid` | query | `string` | no | Filter locations by category, such as ST, CITY, or ZIP. |
