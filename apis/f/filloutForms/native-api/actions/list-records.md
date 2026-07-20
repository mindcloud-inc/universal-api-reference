# List Records with Fillout Forms

Retrieves records from a Fillout table.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/list`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [List Records](https://www.fillout.com/help/database/list-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database. |
| `tableId` | path | `string` | yes | The unique identifier of the table. You can also use the table name instead of the ID. |
| `limit` | body | `number` | no | Number of records to return. Default is 500 and the maximum is 2000. |
| `offset` | body | `number` | no | Number of records to skip for pagination. |
