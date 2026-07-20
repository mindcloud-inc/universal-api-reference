# Update Record with Fillout

Updates a record in Fillout.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Update Record](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `tableId` | path | `string` | yes | The table identifier. |
| `recordId` | path | `string` | yes | The record identifier. |
| `record` | body | `object` | yes | The record payload to update. |
