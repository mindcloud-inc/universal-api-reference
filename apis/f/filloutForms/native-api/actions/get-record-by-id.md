# Get Record by ID with Fillout Forms

Retrieves a record by ID from Fillout.

## Endpoint

- **Method:** `GET`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Get Record by ID](https://www.fillout.com/help/database/get-record-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database. |
| `tableId` | path | `string` | yes | The unique identifier of the table. You can also use the table name instead of the ID. |
| `recordId` | path | `string` | yes | The UUID of the record. |
