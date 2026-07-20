# Delete Row with Stackby

Deletes an existing row from a Stackby table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/betav1/rowdelete/{{stackId}}/{{tableName}}?rowIds[]={{rowId}}`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [Delete Row](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableName` | path | `string` | yes | Table name from Stackby. |
| `rowId` | path | `string` | yes | Stackby row identifier to delete. |
