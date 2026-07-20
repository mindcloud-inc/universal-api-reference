# Search Collection with Needle

Searches a collection in Needle by query.

## Endpoint

- **Method:** `POST`
- **Path:** `https://search.needle.app/api/v1/collections/:collectionId/search`
- **Base URL:** `https://needle.app`
- **Official documentation:** [Search Collection](https://docs.needle.app/docs/api-reference/search-collection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | ID of the collection to search |
| `text` | body | `string` | yes | Search text to query in the collection |
| `top_k` | body | `number` | no | Maximum number of search results to return |
| `offset` | body | `number` | no | Offset to start returning search results from |
