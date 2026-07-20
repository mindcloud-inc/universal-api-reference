# Get Export To File Status In Group with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/reports/[:reportId]/exports/[:exportId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Export To File Status In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-export-to-file-status-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `reportId` | path | `string` | yes | The report ID |
| `exportId` | path | `string` | yes | The export ID |
