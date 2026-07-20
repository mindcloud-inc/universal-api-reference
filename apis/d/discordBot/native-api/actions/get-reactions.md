# Get Reactions with Discord-Bot

Retrieves users who reacted to a Discord message.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:channelId/messages/:messageId/reactions/:emojiName`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Get Reactions](https://docs.discord.com/developers/resources/message#get-reactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return users after this user ID. |
| `channelId` | path | `string` | yes | Discord channel ID. |
| `messageId` | path | `string` | yes | Discord message ID. |
| `emojiName` | path | `string` | yes | URL-encoded emoji identifier. |
