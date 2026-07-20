# List Dashboards in Installed App with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `apps/[:appId]/dashboards`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [List Dashboards in Installed App](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-dashboards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | The installed app ID. |
