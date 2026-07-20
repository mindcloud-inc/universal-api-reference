# Edit Message with Discord-Bot

Updates an existing message in Discord.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/channels/:channelId/messages/:messageId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Edit Message](https://docs.discord.com/developers/resources/message#edit-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Discord channel ID. |
| `messageId` | path | `string` | yes | Discord message ID. |
| `content` | body | `string` | no | New message content. |
