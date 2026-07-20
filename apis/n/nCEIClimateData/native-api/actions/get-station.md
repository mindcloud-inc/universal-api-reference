# Get Station with NCEI Climate Data

Retrieves station details from NCEI Climate Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/stations/[:stationId]`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [Get Station](https://www.ncei.noaa.gov/cdo-web/webservices/v2#stations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stationId` | path | `string` | yes | Station identifier to retrieve, for example COOP:010008. |
