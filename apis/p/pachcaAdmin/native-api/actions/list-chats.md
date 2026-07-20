# List Chats with Pachca (Admin)

Retrieves chats from the Pachca Admin API.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [List Chats](https://dev.pachca.com/api/chats/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `last_message_at_after` | query | `date` | no | Filter chats whose last message was created on or after this timestamp. |
| `last_message_at_before` | query | `date` | no | Filter chats whose last message was created on or before this timestamp. |
| `limit` | query | `number` | no | — |
| `order` | query | `string` | no | Sort direction. |
| `sort` | query | `string` | no | Sort field. |
| `cursor` | query | `string` | no | — |
| `personal` | query | `boolean` | no | — |
| `availability` | query | `string` | no | — |
