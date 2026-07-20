# Delete Table with Fillout Forms

Deletes a table from Fillout.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Delete Table](https://www.fillout.com/help/database/delete-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database |
| `tableId` | path | `string` | yes | The unique identifier of the table. You can also use the table name instead of the ID. |
