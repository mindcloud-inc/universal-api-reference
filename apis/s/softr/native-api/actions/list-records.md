# List Records with Softr

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/:databaseId/tables/:tableId/records`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [List Records](https://docs.softr.io/softr-api/softr-database-api/records/get-records)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database ID that contains the table. |
| `tableId` | path | `string` | yes | The table ID to read records from. |
| `fieldNames` | query | `boolean` | no | Return field names instead of field IDs in the response. |
| `viewId` | query | `string` | no | Limit the response to records from a specific view. |
