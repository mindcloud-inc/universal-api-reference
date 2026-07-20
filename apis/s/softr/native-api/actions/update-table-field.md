# Update Table Field with Softr

## Endpoint

- **Method:** `PUT`
- **Path:** `/databases/:databaseId/tables/:tableId/fields/:fieldId`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Update Table Field](https://docs.softr.io/softr-api/softr-database-api/table-fields/update-table-field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `databaseId` | path | `string` | yes |
| `tableId` | path | `string` | yes |
| `fieldId` | path | `string` | yes |
| `name` | body | `string` | no |
| `type` | body | `string` | no |
| `options` | body | `object` | no |
