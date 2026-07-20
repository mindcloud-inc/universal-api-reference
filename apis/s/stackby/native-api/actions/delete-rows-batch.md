# Delete Rows Batch with Stackby

Deletes existing rows from a Stackby table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/betav1/rowdelete/{{stackId}}/{{tableName}}?{{rowIdsQuery}}`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [Delete Rows Batch](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableName` | path | `string` | yes | Table name from Stackby. |
| `rowIdsQuery` | path | `string` | yes | Exact query string such as rowIds[]=rw123&rowIds[]=rw456. |
