# List Rows Latest with Stackby

Retrieves recently changed rows from a Stackby table.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/rowlist/{{stackId}}/{{tableName}}?latest=true`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [List Rows Latest](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/d7webc7/stackby-extensive-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableName` | path | `string` | yes | Table name from Stackby. |
