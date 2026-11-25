# Query OData Table with Body with Epicor Prophet 21

## Endpoint

- **Method:** `POST`
- **Path:** `/odataservice/odata/table/:tableName/$query`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Query OData Table with Body](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html#long-filters-and-post-query)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tableName` | path | `list<string>` | yes |
| `queryOptions` | body | `string` | yes |
