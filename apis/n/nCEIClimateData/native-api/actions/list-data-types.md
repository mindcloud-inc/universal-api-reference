# List Data Types with NCEI Climate Data

Finds data types in NCEI Climate Data by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/datatypes`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [List Data Types](https://www.ncei.noaa.gov/cdo-web/webservices/v2#data-types)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datacategoryid` | query | `string` | no | Filter data types by data category id, such as TEMP. |
| `datasetid` | query | `string` | no | Filter data types by dataset id, such as GSOM. |
| `locationid` | query | `string` | no | Filter data types by location id. |
| `stationid` | query | `string` | no | Filter data types by station id. |
