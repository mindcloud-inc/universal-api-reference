# List Comments with Yanado

Retrieves comments from Yanado.

## Endpoint

- **Method:** `GET`
- **Path:** `/public-api/comments`
- **Base URL:** `https://api.yanado.com`
- **Official documentation:** [List Comments](https://api.yanado.com/docs/#get-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | query | `string` | no | Filter comments by list ID. |
| `query` | query | `string` | no | Search comments by query text. |
