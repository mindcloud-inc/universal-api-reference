# Get Report Page with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/reports/[:reportId]/pages/[:pageName]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Report Page](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-page-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID. |
| `reportId` | path | `string` | yes | The report ID. |
| `pageName` | path | `string` | yes | The report page name. |
