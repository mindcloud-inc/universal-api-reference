# List Table Columns with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `GET`
- **Path:** `/EntityDefinitions(LogicalName=':logicalName')/Attributes`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [List Table Columns](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/query-metadata-web-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logicalName` | path | `string` | yes | LogicalName returned by List Tables, such as account or new_project. |
| `$select` | query | `string` | no | — |
| `$filter` | query | `string` | no | Optional filter on column metadata. |
