# Get Refreshable For Capacity with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/capacities/[:capacityId]/refreshables/[:refreshableId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Refreshable For Capacity](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/get-refreshable-for-capacity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capacityId` | path | `string` | yes | The capacity ID |
| `refreshableId` | path | `string` | yes | The refreshable ID |
| `$expand` | query | `string` | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports capacities and groups. |
