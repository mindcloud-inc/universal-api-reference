# Delete Report in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `groups/[:groupId]/reports/[:reportId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Delete Report in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/delete-report-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `reportId` | path | `string` | yes | The report ID to delete. |
