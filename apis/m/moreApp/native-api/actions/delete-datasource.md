# Delete Datasource with MoreApp

Deletes a datasource from MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1.0/customers/{{customerId}}/datasources/{{dataSourceId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Delete Datasource](https://docs.moreapp.com/docs/developer-docs/a3de527c2edad-delete-a-datasource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer ID. |
| `dataSourceId` | path | `string` | yes | Datasource ID. |
