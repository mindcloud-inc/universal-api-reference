# Update Datasources In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/reports/[:reportId]/Default.UpdateDatasources`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Datasources In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/update-datasources-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `reportId` | path | `string` | yes | The report ID |
| `updateDetails[]` | body | `array<object>` | yes | The update details for the data sources of the paginated report |
