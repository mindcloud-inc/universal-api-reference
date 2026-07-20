# Groups GetGroupsAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/groups`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Groups GetGroupsAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-get-groups-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | yes | Returns only the first n results. This parameter is mandatory and must be in the range of 1-5000. |
| `$expand` | query | `string` | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports users, reports, dashboards, datasets, dataflows, and workbooks. |
| `$filter` | query | `string` | no | Returns a subset of a results based on Odata filter query parameter condition. |
| `$skip` | query | `number` | no | Skips the first n results. Use with top to fetch results beyond the first 5000. |
