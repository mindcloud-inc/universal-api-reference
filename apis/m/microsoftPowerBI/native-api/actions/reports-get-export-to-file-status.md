# Get Export To File Status with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `reports/[:reportId]/exports/[:exportId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Export To File Status](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-export-to-file-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `string` | yes | The report ID |
| `exportId` | path | `string` | yes | The export ID |
