# Soft Delete Chat Message with Microsoft Teams

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/users/:userId/chats/:chatId/messages/:messageId/softDelete`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Soft Delete Chat Message](https://learn.microsoft.com/en-us/graph/api/chatmessage-softdelete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userId` | path | `string` | yes |
| `chatId` | path | `string` | yes |
| `messageId` | path | `string` | yes |
