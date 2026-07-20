# Delete Dashboard in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `groups/[:groupId]/dashboards/[:dashboardId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Delete Dashboard in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/delete-dashboard-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `dashboardId` | path | `string` | yes | The dashboard ID to delete. |
