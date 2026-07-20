# Calculate Text-to-Embedding Price with deAPI

Calculates text-to-embedding request pricing in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/txt2embedding/price-calculation`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | no | Text or text array to price for embeddings. |
| `model` | body | `string` | no | Embedding model slug from List Models. |
