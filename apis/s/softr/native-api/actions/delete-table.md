# Delete Table with Softr

## Endpoint

- **Method:** `DELETE`
- **Path:** `/databases/:databaseId/tables/:tableId`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Delete Table](https://docs.softr.io/softr-api/softr-database-api/tables/delete-table)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `databaseId` | path | `string` | yes |
| `tableId` | path | `string` | yes |
| `force` | query | `boolean` | no |
