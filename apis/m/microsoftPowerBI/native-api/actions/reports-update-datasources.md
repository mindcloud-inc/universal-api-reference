# Update Datasources with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `reports/[:reportId]/Default.UpdateDatasources`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Datasources](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/update-datasources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `string` | yes | The report ID |
| `updateDetails[]` | body | `array<object>` | yes | The update details for the data sources of the paginated report |
