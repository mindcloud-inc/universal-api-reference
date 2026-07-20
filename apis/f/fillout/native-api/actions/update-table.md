# Update Table with Fillout

Updates a table in Fillout.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Update Table](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `name` | body | `string` | no | The updated table name. |
| `tableId` | path | `string` | yes | The table identifier. |
