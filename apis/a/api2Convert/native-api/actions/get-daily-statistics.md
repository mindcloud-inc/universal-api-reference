# Get Daily Statistics with Api2Convert

Retrieves statistics for a specific day from Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/stats/day/:day/:filter`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Get Daily Statistics](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `day` | path | `string` | yes | Day in yyyy-mm-dd format. |
| `filter` | path | `string` | yes | Statistics scope filter: single or all. Accepted values: `0`, `1`. |
