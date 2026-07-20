# Delete a Table with Quickbase

Deletes an existing table from Quickbase.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v1/tables/:tableId`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Delete a Table](https://developer.quickbase.com/operation/deleteTable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | query | `string` | yes | The Quickbase app that owns the table. |
| `tableId` | path | `string` | yes | The Quickbase table to delete. |
