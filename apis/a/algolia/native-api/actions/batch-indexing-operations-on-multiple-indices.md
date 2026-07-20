# Batch Indexing Operations on Multiple Indices with Algolia

Runs batch indexing operations on multiple Algolia indices.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/*/batch`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Batch Indexing Operations on Multiple Indices](https://www.algolia.com/doc/rest-api/search/multiple-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requests[]` | body | `array<object>` | yes | Batch requests for one or more indices. |
