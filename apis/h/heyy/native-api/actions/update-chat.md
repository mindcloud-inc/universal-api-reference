# Update Chat with Heyy

Updates an existing chat in a Heyy channel.

## Endpoint

- **Method:** `PUT`
- **Path:** `/[:channelId]/chats/:chatId`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Update Chat](https://docs.heyy.io/api-reference/update-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignedTeamId` | body | `string` | no | The assigned team ID. |
| `assignedUserId` | body | `string` | no | The assigned user ID. |
| `channelId` | path | `string` | yes | The channel ID. |
| `chatId` | path | `string` | yes | The chat ID. |
| `isUnread` | body | `boolean` | no | Whether the chat should be marked unread. |
| `status` | body | `string` | no | The chat status. |
