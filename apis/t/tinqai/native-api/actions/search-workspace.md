# Search Workspace with Tinq.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/search`
- **Base URL:** `https://tinq.ai`
- **Official documentation:** [Search Workspace](https://docs.tinq.ai/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search query text. |
| `top_k` | body | `number` | no | Maximum number of results to return. |
