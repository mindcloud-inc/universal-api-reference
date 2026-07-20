# Update Record with Fillout Forms

Updates an existing record in Fillout.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Update Record](https://www.fillout.com/help/database/update-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database. |
| `tableId` | path | `string` | yes | The unique identifier of the table. You can also use the table name instead of the ID. |
| `recordId` | path | `string` | yes | The UUID of the record to update. |
| `record` | body | `object` | yes | Fields to update with their new values. Only include fields you want to change. |
