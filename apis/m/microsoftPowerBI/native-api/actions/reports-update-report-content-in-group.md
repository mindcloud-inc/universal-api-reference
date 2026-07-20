# Update Report Content In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/reports/[:reportId]/UpdateReportContent`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Report Content In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/update-report-content-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `reportId` | path | `string` | yes | The report ID |
| `sourceReport` | body | `object` | yes | An existing source report |
| `sourceType` | body | `object` | yes | The source type of the content update |
