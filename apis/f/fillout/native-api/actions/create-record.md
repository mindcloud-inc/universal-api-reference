# Create Record with Fillout

Creates a new record in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Create Record](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `tableId` | path | `string` | yes | The table identifier. |
| `record` | body | `object` | yes | The record payload to create. |
