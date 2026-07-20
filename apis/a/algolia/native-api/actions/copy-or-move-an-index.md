# Copy or Move an Index with Algolia

Copies or moves an Algolia index.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/operation`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Copy or Move an Index](https://www.algolia.com/doc/rest-api/search/operation-index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The source Algolia index. |
| `operation` | body | `list` | yes | Whether to copy or move the index. Accepted values: `0`, `1`. |
| `destination` | body | `string` | yes | Destination index name. |
| `scope[]` | body | `array<string>` | no | Scopes to copy when using the copy operation. |
