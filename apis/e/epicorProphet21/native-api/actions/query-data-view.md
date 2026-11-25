# Query Data View with Epicor Prophet 21

## Endpoint

- **Method:** `GET`
- **Path:** `/data/erp/views/v1/:view`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Query Data View](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html#the-other-odata-surface-data-erp-views-v1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view` | path | `string` | yes | The Prophet 21 data view name, such as p21_view_customer. |
| `$select` | query | `string` | no | Comma-separated field names. Leave empty to return all available fields. |
| `$filter` | query | `string` | no | A Prophet 21 filter expression, such as customer_id eq 123. |
| `$inlinecount` | query | `list<string>` | no | Accepted values: `allpages`, `none`. Format: `toggle`. |
