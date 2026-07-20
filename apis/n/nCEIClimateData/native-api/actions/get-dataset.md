# Get Dataset with NCEI Climate Data

Retrieves dataset details from NCEI Climate Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasets/[:datasetId]`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [Get Dataset](https://www.ncei.noaa.gov/cdo-web/webservices/v2#datasets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | Dataset identifier to retrieve, for example GHCND. |
