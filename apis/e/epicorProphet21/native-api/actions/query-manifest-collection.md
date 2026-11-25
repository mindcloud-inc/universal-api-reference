# Query Manifest Collection with Epicor Prophet 21

## Endpoint

- **Method:** `GET`
- **Path:** `/data/manifest/v1/:collection`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Query Manifest Collection](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html)

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
| `collection` | path | `list<string>` | yes | — |
| `$select` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `$filter` | query | `string` | no | OData filter expression. Quote string values and double embedded single quotes. Combine values with or; do not use in, which can be silently ignored. |
| `$inlinecount` | query | `list<string>` | no | Accepted values: `allpages`, `none`. |
