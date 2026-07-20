# Delete Record with Fillout

Deletes a record from Fillout.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Delete Record](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `tableId` | path | `string` | yes | The table identifier. |
| `recordId` | path | `string` | yes | The record identifier. |
