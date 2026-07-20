# Reports GetReportsAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/reports`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Reports GetReportsAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/reports-get-reports-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Returns a subset of a results based on Odata filter query parameter condition. |
| `$skip` | query | `number` | no | Skips the first n results |
| `$top` | query | `number` | no | Returns only the first n results |
