# Search Content in Collection with Grok

Finds content in a Grok collection by search query.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents/search`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Search Content in Collection](https://docs.x.ai/developers/rest-api-reference/collections/search#search-content-in-a-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search query text. |
| `source.collection_ids[]` | body | `array<string>` | no | Collection IDs to search within. |
| `filter` | body | `string` | no | Optional filter expression. |
