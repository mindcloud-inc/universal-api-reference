# Export Report In Group with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/reports/[:reportId]/Export`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Export Report In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/export-report-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `reportId` | path | `string` | yes | The report ID |
| `downloadType` | query | `object` | no | The type of download. Valid values are LiveConnect and IncludeModel |
