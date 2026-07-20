# Get Monthly Statistics with Api2Convert

Retrieves statistics for a specific month from Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/stats/month/:month/:filter`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Get Monthly Statistics](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `month` | path | `string` | yes | Month in yyyy-mm format. |
| `filter` | path | `string` | yes | Statistics scope filter: single or all. Accepted values: `0`, `1`. |
