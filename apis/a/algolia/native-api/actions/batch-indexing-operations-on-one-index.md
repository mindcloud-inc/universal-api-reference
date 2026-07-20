# Batch Indexing Operations on One Index with Algolia

Runs batch indexing operations on one Algolia index.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/batch`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Batch Indexing Operations on One Index](https://www.algolia.com/doc/rest-api/search/batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |
| `requests[]` | body | `array<object>` | yes | Batch requests for the index. |
