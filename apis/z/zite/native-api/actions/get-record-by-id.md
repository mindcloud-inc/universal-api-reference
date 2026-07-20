# Get Record by ID with Zite

Retrieves a specific record from Zite by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/bases/:databaseId/tables/:tableId/records/:recordId`
- **Base URL:** `https://tables.fillout.com/api/v1`
- **Official documentation:** [Get Record by ID](https://fillout.com/help/database/get-record-by-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `databaseId` | path | `string` | yes |
| `recordId` | path | `string` | yes |
| `tableId` | path | `string` | yes |
