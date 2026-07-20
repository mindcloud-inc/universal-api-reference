# List chat messages with YouGile

Retrieves chat messages from a YouGile chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/:chatId/messages`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [List chat messages](https://ru.yougile.com/api-v2#/operations/ChatMessageController_search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The YouGile chat ID. |
| `includeDeleted` | query | `boolean` | no | Include deleted messages in the result. |
| `fromUserId` | query | `string` | no | Filter messages by sender user ID. |
| `text` | query | `string` | no | Filter messages by text. |
| `label` | query | `string` | no | Filter messages by label. |
| `since` | query | `number` | no | Return messages updated since this timestamp. |
| `includeSystem` | query | `boolean` | no | Include system messages in the result. |
