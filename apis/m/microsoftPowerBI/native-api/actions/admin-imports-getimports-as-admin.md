# Imports GetImportsAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/imports`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Imports GetImportsAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/imports-get-imports-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$expand` | query | `string` | no | Expands related entities inline |
| `$filter` | query | `string` | no | Returns a subset of a results based on Odata filter query parameter condition. |
| `$skip` | query | `number` | no | Skips the first n results |
| `$top` | query | `number` | no | Returns only the first n results |
