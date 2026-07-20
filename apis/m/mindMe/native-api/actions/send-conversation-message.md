# Send Conversation Message with MindMe

Creates a new conversation message in MindMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Conversation/SendConversationMessage`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [Send Conversation Message](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Conversation~1SendConversationMessage/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `conversationStartId` | body | `string` | no |
| `inboxId` | body | `string` | no |
| `messageBody` | body | `string` | no |
| `parentAccountId` | body | `string` | no |
| `sendOption` | body | `string` | no |
| `subAccountId` | body | `string` | no |
| `userId` | body | `string` | no |
