# List Records with Zite

Retrieves records from a specific Zite table.

## Endpoint

- **Method:** `POST`
- **Path:** `/bases/:databaseId/tables/:tableId/records/list`
- **Base URL:** `https://tables.fillout.com/api/v1`
- **Official documentation:** [List Records](https://fillout.com/help/database/list-records)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `databaseId` | path | `string` | yes |
| `tableId` | path | `string` | yes |
