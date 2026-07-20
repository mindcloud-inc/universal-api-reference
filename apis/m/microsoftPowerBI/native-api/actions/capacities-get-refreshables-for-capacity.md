# Get Refreshables For Capacity with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `capacities/[:capacityId]/refreshables`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Refreshables For Capacity](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/get-refreshables-for-capacity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capacityId` | path | `string` | yes | The capacity ID |
| `$top` | query | `number` | yes | Returns only the first n results. |
| `$expand` | query | `string` | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports capacities and groups. |
| `$filter` | query | `string` | no | Returns a subset of a results based on Odata filter query parameter condition. |
| `$skip` | query | `number` | no | Skips the first n results. Use with top to fetch results beyond the first 1000. |
