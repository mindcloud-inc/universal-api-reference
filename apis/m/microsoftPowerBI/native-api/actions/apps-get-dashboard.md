# Get Dashboard with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `apps/[:appId]/dashboards/[:dashboardId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Dashboard](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-dashboard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | The app ID |
| `dashboardId` | path | `string` | yes | The dashboard ID |
