# List Location Categories with NCEI Climate Data

Finds location categories in NCEI Climate Data by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/locationcategories`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [List Location Categories](https://www.ncei.noaa.gov/cdo-web/webservices/v2#location-categories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetid` | query | `string` | no | Filter location categories by dataset id, such as GSOM. |
