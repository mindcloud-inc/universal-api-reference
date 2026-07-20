# Get Tiles with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `apps/[:appId]/dashboards/[:dashboardId]/tiles`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Tiles](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-tiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | The app ID |
| `dashboardId` | path | `string` | yes | The dashboard ID |
