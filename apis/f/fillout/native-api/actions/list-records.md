# List Records with Fillout

Retrieves records from Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/list`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [List Records](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `tableId` | path | `string` | yes | The table identifier. |
| `limit` | body | `number` | no | Optional page size. |
| `offset` | body | `number` | no | Optional pagination offset. |
| `sort[]` | body | `array<object>` | no | Optional sort descriptors. |
| `filter` | body | `object` | no | Optional filter object. |
