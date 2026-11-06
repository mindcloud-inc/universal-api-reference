# List Tables with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `GET`
- **Path:** `/EntityDefinitions`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [List Tables](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/query-metadata-web-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `string` | no | — |
| `$filter` | query | `string` | no | Use IsCustomEntity eq true to list only custom tables. |
