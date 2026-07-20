# Get Latest Series Data with Bureau of Labor Statistics

Retrieves the latest data point for a Bureau of Labor Statistics series.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeseries/data/:seriesId`
- **Base URL:** `https://api.bls.gov/publicAPI/v2`
- **Official documentation:** [Get Latest Series Data](https://www.bls.gov/developers/api_signature_v2.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `seriesId` | path | `string` | yes | BLS time series ID. Use uppercase BLS format, for example LAUCN040010000000005. |
