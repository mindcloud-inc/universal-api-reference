# Create Record with Softr

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/:databaseId/tables/:tableId/records`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Create Record](https://docs.softr.io/softr-api/softr-database-api/records/create-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database ID that contains the table. |
| `tableId` | path | `string` | yes | The table ID to create the record in. |
| `fieldNames` | query | `boolean` | no | Return field names instead of field IDs in the response. |
| `fields` | body | `object` | yes | The field values to create on the record. |
