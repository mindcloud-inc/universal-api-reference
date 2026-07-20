# Paginate Rows with Stackby

Retrieves paginated rows from a Stackby table.

## Endpoint

- **Method:** `GET`
- **Path:** `/betav1/rowlist/{{stackId}}/{{tableName}}`
- **Base URL:** `https://stackby.com/api`
- **Official documentation:** [Paginate Rows](https://www.postman.com/lively-equinox-180638/stackby-s-public-workspace/documentation/bmmadzn/stackby-developer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stackId` | path | `string` | yes | Stack identifier from Stackby. |
| `tableName` | path | `string` | yes | Table name from Stackby. |
| `pageSize` | query | `number` | no | Maximum rows returned in this page. |
| `offset` | query | `number` | no | Row offset for pagination. |
