# Get Data View Record with Epicor Prophet 21

## Endpoint

- **Method:** `GET`
- **Path:** `/data/erp/views/v1/:view(:key)`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Get Data View Record](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view` | path | `list<string>` | yes | — |
| `key` | path | `string` | yes | OData key expression, including quotes for string keys. For compound keys, name each part and preserve its documented type. |
| `$select` | query | `string` | no | Send multiple values as a string separated by `,`. |
