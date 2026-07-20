# Add Table Field with Softr

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/:databaseId/tables/:tableId/fields`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Add Table Field](https://docs.softr.io/softr-api/softr-database-api/table-fields/add-table-field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `databaseId` | path | `string` | yes |
| `tableId` | path | `string` | yes |
| `name` | body | `string` | yes |
| `type` | body | `string` | yes |
| `options` | body | `object` | no |
