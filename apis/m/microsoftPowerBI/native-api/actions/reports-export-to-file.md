# Export To File with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `reports/[:reportId]/ExportTo`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Export To File](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/export-to-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `string` | yes | The report ID |
| `format` | body | `object` | yes | The requested format for the exported file |
| `paginatedReportConfiguration` | body | `object` | no | The configuration used to export a paginated report |
| `powerBIReportConfiguration` | body | `object` | no | The configuration used to export a Power BI report |
