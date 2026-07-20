# Get Page with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `reports/[:reportId]/pages/[:pageName]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Page](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `string` | yes | The report ID |
| `pageName` | path | `string` | yes | The page name |
