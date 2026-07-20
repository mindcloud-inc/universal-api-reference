# Rebind Report with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `reports/[:reportId]/Rebind`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Rebind Report](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/rebind-report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `string` | yes | The report ID |
| `datasetId` | body | `string` | yes | The new dataset for the rebound report. If the dataset resides in a different workspace than the report, a shared dataset will be created in the report's workspace. |
