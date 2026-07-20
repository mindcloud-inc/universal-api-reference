# Search an Index with Algolia

Searches one Algolia index for matching records.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/query`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Search an Index](https://www.algolia.com/doc/rest-api/search/search-single-index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index to search. |
| `params` | body | `string` | no | URL-encoded Algolia search parameters. |
