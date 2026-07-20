# List Dashboard Tiles with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/dashboards/[:dashboardId]/tiles`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [List Dashboard Tiles](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-tiles-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID. |
| `dashboardId` | path | `string` | yes | The dashboard ID. |
