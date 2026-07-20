# Get Location with NCEI Climate Data

Retrieves location details from NCEI Climate Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/[:locationId]`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [Get Location](https://www.ncei.noaa.gov/cdo-web/webservices/v2#locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | yes | Location identifier to retrieve, for example FIPS:37 or ZIP:28801. |
