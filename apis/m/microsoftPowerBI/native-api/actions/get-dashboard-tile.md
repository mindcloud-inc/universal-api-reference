# Get Dashboard Tile with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/dashboards/[:dashboardId]/tiles/[:tileId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Dashboard Tile](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-tile-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID. |
| `dashboardId` | path | `string` | yes | The dashboard ID. |
| `tileId` | path | `string` | yes | The tile ID. |
