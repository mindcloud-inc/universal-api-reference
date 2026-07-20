# Get Dashboard in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/dashboards/[:dashboardId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Dashboard in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-dashboard-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID. |
| `dashboardId` | path | `string` | yes | The dashboard ID. |
