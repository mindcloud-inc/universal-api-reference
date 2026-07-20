# Update Row with Stackby

Updates an existing row in a Stackby table.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/betav1/rowupdate/{{stackId}}/{{tableName}}`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [Update Row](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableName` | path | `string` | yes | Table name from Stackby. |
| `records` | body | `list<object>` | yes | Records array containing one row id and field patch. |
