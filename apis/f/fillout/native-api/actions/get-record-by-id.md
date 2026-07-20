# Get Record By Id with Fillout

Retrieves a record from Fillout by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Get Record By Id](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `tableId` | path | `string` | yes | The table identifier. |
| `recordId` | path | `string` | yes | The record identifier. |
