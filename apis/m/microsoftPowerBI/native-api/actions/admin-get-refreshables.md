# Get Refreshables with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/capacities/refreshables`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Refreshables](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/get-refreshables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | yes | Returns only the first n results. |
| `$expand` | query | `string` | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports capacities and groups. |
| `$filter` | query | `string` | no | Returns a subset of a results based on Odata filter query parameter condition. |
| `$skip` | query | `number` | no | Skips the first n results. Use with top to fetch results beyond the first 1000. |
