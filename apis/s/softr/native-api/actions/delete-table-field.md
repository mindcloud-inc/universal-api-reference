# Delete Table Field with Softr

## Endpoint

- **Method:** `DELETE`
- **Path:** `/databases/:databaseId/tables/:tableId/fields/:fieldId`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Delete Table Field](https://docs.softr.io/softr-api/softr-database-api/table-fields/delete-table-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database ID that contains the table. |
| `tableId` | path | `string` | yes | The table ID that contains the field. |
| `fieldId` | path | `string` | yes | The field ID to delete. |
