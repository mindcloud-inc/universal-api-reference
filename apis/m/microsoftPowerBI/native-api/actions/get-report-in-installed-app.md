# Get Report in Installed App with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `apps/[:appId]/reports/[:reportId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Report in Installed App](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | The installed app ID. |
| `reportId` | path | `string` | yes | The report ID. |
