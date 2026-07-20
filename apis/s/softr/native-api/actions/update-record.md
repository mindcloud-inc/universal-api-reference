# Update Record with Softr

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/:databaseId/tables/:tableId/records/:recordId`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Update Record](https://docs.softr.io/softr-api/softr-database-api/records/update-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database ID that contains the table. |
| `tableId` | path | `string` | yes | The table ID that contains the record. |
| `recordId` | path | `string` | yes | The record ID to update. |
| `fieldNames` | query | `boolean` | no | Return field names instead of field IDs in the response. |
| `fields` | body | `object` | yes | The field values to update on the record. |
