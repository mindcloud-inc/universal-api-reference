# Groups GetGroupAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/groups/[:groupId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Groups GetGroupAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-get-group-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `$expand` | query | `string` | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports users, reports, dashboards, datasets, dataflows, and workbooks. |
