# Get Rows By ID with Stackby

Retrieves Stackby rows by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/betav1/rowlist/{{stackId}}/{{tableName}}?{{rowIdsQuery}}`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [Get Rows By ID](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableName` | path | `string` | yes | Table name from Stackby. |
| `rowIdsQuery` | path | `string` | yes | Exact query string such as rowIds[]=rw123&rowIds[]=rw456. |
