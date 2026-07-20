# List Columns with Stackby

Retrieves columns from a Stackby table.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/columnlist/{{stackId}}/{{tableId}}`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [List Columns](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/d7webc7/stackby-extensive-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableId` | path | `string` | yes | Table identifier from Stackby. |
