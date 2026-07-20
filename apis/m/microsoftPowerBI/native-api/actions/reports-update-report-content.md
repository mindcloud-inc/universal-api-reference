# Update Report Content with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `reports/[:reportId]/UpdateReportContent`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Report Content](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/update-report-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `string` | yes | The report ID |
| `sourceReport` | body | `object` | yes | An existing source report |
| `sourceType` | body | `object` | yes | The source type of the content update |
