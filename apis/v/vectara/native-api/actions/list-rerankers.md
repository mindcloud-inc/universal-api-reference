# List Rerankers with Vectara

Retrieves the available rerankers from Vectara.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/rerankers`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [List Rerankers](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Regex filter against reranker names and descriptions. |
| `limit` | query | `number` | no | Maximum number of rerankers to return. |
| `page_key` | query | `string` | no | Cursor for the next page of rerankers. |
