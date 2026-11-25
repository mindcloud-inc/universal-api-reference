# Query OData View with Body with Epicor Prophet 21

## Endpoint

- **Method:** `POST`
- **Path:** `/odataservice/odata/view/:viewName/$query`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Query OData View with Body](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `viewName` | path | `list<string>` | yes |
| `queryOptions` | body | `string` | yes |
