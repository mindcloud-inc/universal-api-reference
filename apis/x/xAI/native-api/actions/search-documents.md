# Search Documents with xAI

Finds documents in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/search`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Search Documents](https://docs.x.ai/developers/rest-api-reference/collections/search#search-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Query text to search for across collections. |
| `source` | body | `object` | no | Source object containing collection_ids to search. |
| `limit` | body | `number` | no | Number of chunks to return. |
