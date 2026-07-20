# Create Row with Stackby

Creates a new row in a Stackby table.

## Endpoint

- **Method:** `POST`
- **Path:** `/betav1/rowcreate/{{stackId}}/{{tableName}}`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [Create Row](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableName` | path | `string` | yes | Table name from Stackby. |
| `records` | body | `list<object>` | yes | Records array containing one field object. |
