# List Conversation Messages with MindMe

Retrieves conversation messages from MindMe.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Conversation/GetConversationMessages`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [List Conversation Messages](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Conversation~1GetConversationMessages/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `conversationStartId` | query | `string` | no |
| `inboxId` | query | `string` | no |
| `userId` | query | `string` | no |
