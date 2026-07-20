# Search with Moorcheh

Finds relevant results in Moorcheh across selected namespaces.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Search](https://docs.moorcheh.ai/api-reference/search/query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search query text. Metadata and keyword filters can be placed at the end of the query using Moorcheh syntax. |
| `namespaces[]` | body | `array<string>` | yes | Array of namespace names to search. All namespaces must be of the same type. |
| `top_k` | body | `number` | no | Number of top relevant chunks to return. Defaults to 10 in Moorcheh. |
| `kiosk_mode` | body | `boolean` | no | When enabled, Moorcheh filters chunks below the threshold. |
| `threshold` | body | `number` | no | Minimum relevance score from 0 to 1. Required by Moorcheh when kiosk mode is enabled. |
