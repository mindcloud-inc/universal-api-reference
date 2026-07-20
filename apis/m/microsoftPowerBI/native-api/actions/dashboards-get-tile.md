# Get Tile with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `dashboards/[:dashboardId]/tiles/[:tileId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Tile](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-tile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dashboardId` | path | `string` | yes | The dashboard ID |
| `tileId` | path | `string` | yes | The tile ID |
