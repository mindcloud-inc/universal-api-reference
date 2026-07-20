# List Stations with NCEI Climate Data

Finds weather stations in NCEI Climate Data by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/stations`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [List Stations](https://www.ncei.noaa.gov/cdo-web/webservices/v2#stations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetid` | query | `string` | no | Filter stations by dataset id, such as GHCND. |
| `datatypeid` | query | `string` | no | Filter stations by data type id, such as TAVG. |
| `extent` | query | `string` | no | Geographic bounding box as south,west,north,east coordinates. |
| `locationid` | query | `string` | no | Filter stations by location id, such as FIPS:37. |
