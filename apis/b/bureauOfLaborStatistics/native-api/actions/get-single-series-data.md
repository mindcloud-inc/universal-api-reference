# Get Single Series Data with Bureau of Labor Statistics

Retrieves recent data for one Bureau of Labor Statistics series.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeseries/data/:seriesId`
- **Base URL:** `https://api.bls.gov/publicAPI/v2`
- **Official documentation:** [Get Single Series Data](https://www.bls.gov/developers/api_signature_v2.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `seriesId` | path | `string` | yes | BLS time series ID. Use uppercase BLS format, for example LAUCN040010000000005. |
