# Create Text-to-Embedding Job with deAPI

Creates a text-to-embedding job in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/txt2embedding`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | no | Text or text array to embed. |
| `model` | body | `string` | no | Embedding model slug from List Models. |
| `return_result_in_response` | body | `string` | no | Return embeddings inline instead of just a request id when supported. |
