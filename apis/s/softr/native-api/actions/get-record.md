# Get Record with Softr

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/:databaseId/tables/:tableId/records/:recordId`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Get Record](https://docs.softr.io/softr-api/softr-database-api/records/get-single-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database ID that contains the table. |
| `tableId` | path | `string` | yes | The table ID that contains the record. |
| `recordId` | path | `string` | yes | The record ID to retrieve. |
| `fieldNames` | query | `boolean` | no | Return field names instead of field IDs in the response. |
