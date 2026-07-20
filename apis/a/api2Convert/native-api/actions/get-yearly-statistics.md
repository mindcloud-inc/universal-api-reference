# Get Yearly Statistics with Api2Convert

Retrieves statistics for a specific year from Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/stats/year/:year/:filter`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Get Yearly Statistics](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `string` | yes | Year in yyyy format. |
| `filter` | path | `string` | yes | Statistics scope filter: single or all. Accepted values: `0`, `1`. |
