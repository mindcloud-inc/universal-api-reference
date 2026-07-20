# Export To File In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/reports/[:reportId]/ExportTo`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Export To File In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/export-to-file-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `reportId` | path | `string` | yes | The report ID |
| `format` | body | `object` | yes | The requested format for the exported file |
| `paginatedReportConfiguration` | body | `object` | no | The configuration used to export a paginated report |
| `powerBIReportConfiguration` | body | `object` | no | The configuration used to export a Power BI report |
