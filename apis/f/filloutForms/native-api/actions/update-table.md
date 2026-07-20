# Update Table with Fillout Forms

Updates an existing table in Fillout.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Update Table](https://www.fillout.com/help/database/update-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database |
| `tableId` | path | `string` | yes | The unique identifier of the table. You can also use the table name instead of the ID. |
| `name` | body | `string` | no | New table name |
