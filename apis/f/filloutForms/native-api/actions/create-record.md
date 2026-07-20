# Create Record with Fillout Forms

Creates a record in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Create Record](https://www.fillout.com/help/database/create-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database. |
| `tableId` | path | `string` | yes | The unique identifier of the table. You can also use the table name instead of the ID. |
| `record` | body | `object` | yes | Record data with field names or field IDs as keys and their corresponding values. |
