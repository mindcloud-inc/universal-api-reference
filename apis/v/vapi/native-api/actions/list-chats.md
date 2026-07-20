# List Chats with Vapi

Retrieves a list of chats from Vapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [List Chats](https://docs.vapi.ai/api-reference/chats/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | This is the unique identifier for the chat to filter by. |
| `assistantId` | query | `string` | no | This is the unique identifier for the assistant that will be used for the chat. |
| `assistantIdAny` | query | `string` | no | Filter by multiple assistant IDs. Provide as comma-separated values. |
| `squadId` | query | `string` | no | This is the unique identifier for the squad that will be used for the chat. |
| `sessionId` | query | `string` | no | This is the unique identifier for the session that will be used for the chat. |
| `previousChatId` | query | `string` | no | This is the unique identifier for the previous chat to filter by. |
| `page` | query | `number` | no | This is the page number to return. Defaults to 1. |
| `sortOrder` | query | `string` | no | This is the sort order for pagination. Defaults to 'DESC'. |
| `limit` | query | `number` | no | This is the maximum number of items to return. Defaults to 100. |
| `createdAtGt` | query | `string` | no | This will return items where the createdAt is greater than the specified value. |
| `createdAtLt` | query | `string` | no | This will return items where the createdAt is less than the specified value. |
| `createdAtGe` | query | `string` | no | This will return items where the createdAt is greater than or equal to the specified value. |
| `createdAtLe` | query | `string` | no | This will return items where the createdAt is less than or equal to the specified value. |
| `updatedAtGt` | query | `string` | no | This will return items where the updatedAt is greater than the specified value. |
| `updatedAtLt` | query | `string` | no | This will return items where the updatedAt is less than the specified value. |
| `updatedAtGe` | query | `string` | no | This will return items where the updatedAt is greater than or equal to the specified value. |
| `updatedAtLe` | query | `string` | no | This will return items where the updatedAt is less than or equal to the specified value. |
