# List Direct Chats with Zoho Cliq

Retrieves direct chats from Zoho Cliq.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [List Direct Chats](https://www.zoho.com/cliq/help/restapi/v2/#retrieve-chats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of chats to retrieve. Maximum 100. |
| `modified_before` | query | `string` | no | Only include chats whose last message was sent before this time. |
| `modified_after` | query | `string` | no | Only include chats whose last message was sent after this time. |
| `drafts` | query | `boolean` | no | When true, only chats containing drafts are returned. |
