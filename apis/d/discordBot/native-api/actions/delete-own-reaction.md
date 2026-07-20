# Delete Own Reaction with Discord-Bot

Deletes the bot's reaction from a Discord message.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/channels/:channelId/messages/:messageId/reactions/:emojiName/@me`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Delete Own Reaction](https://docs.discord.com/developers/resources/message#delete-own-reaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Discord channel ID. |
| `messageId` | path | `string` | yes | Discord message ID. |
| `emojiName` | path | `string` | yes | URL-encoded emoji identifier. |
