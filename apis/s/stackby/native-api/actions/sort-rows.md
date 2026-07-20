# Sort Rows with Stackby

Retrieves sorted rows from a Stackby table.

## Endpoint

- **Method:** `GET`
- **Path:** `/betav1/rowlist/{{stackId}}/{{tableName}}`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [Sort Rows](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableName` | path | `string` | yes | Table name from Stackby. |
| `sort` | query | `string` | yes | Stackby sort payload, for example [{field:"Name",direction:"desc"}]. |
