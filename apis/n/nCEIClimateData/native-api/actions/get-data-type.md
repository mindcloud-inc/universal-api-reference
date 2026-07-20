# Get Data Type with NCEI Climate Data

Retrieves data type details from NCEI Climate Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/datatypes/[:dataTypeId]`
- **Base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`
- **Official documentation:** [Get Data Type](https://www.ncei.noaa.gov/cdo-web/webservices/v2#data-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataTypeId` | path | `string` | yes | Data type identifier to retrieve, for example TAVG. |
