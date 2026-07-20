# List Views with Stackby

Retrieves views from a Stackby table.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/viewlist/{{stackId}}/{{tableId}}`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [List Views](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableId` | path | `string` | yes | Table identifier from Stackby. |
