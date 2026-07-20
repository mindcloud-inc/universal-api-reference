# Get File Of Export To File with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `reports/[:reportId]/exports/[:exportId]/file`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get File Of Export To File](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-file-of-export-to-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `string` | yes | The report ID |
| `exportId` | path | `string` | yes | The export ID |
