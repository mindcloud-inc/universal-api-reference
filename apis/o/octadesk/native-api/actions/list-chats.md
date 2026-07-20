# List Chats with Octadesk

Retrieves chats from Octadesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Chats](https://developers.octadesk.com/reference/getchatbyfilter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Limit of items per page. MAX = 100, MIN = 1. |
| `page` | query | `string` | no | Number of the page. Defaults to 1. |
