# Filter Rows with Stackby

Finds rows in a Stackby table by filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/betav1/rowlist/{{stackId}}/{{tableName}}`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [Filter Rows](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableName` | path | `string` | yes | Table name from Stackby. |
| `filter` | query | `string` | yes | Stackby filter expression such as toContains({Status},Todo). |
