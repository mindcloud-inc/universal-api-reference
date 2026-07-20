# Delete Field with Fillout Forms

Deletes a field from Fillout.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields/:fieldId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Delete Field](https://www.fillout.com/help/database/delete-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database |
| `tableId` | path | `string` | yes | The unique identifier of the table. You can also use the table name instead of the ID. |
| `fieldId` | path | `string` | yes | The unique identifier of the field. You can also use the field name instead of the ID. Note: You cannot delete the primary field (the first field in a table). |
