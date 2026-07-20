# Create Reaction with Discord-Bot

Creates a reaction on a Discord message.

## Endpoint

- **Method:** `PUT`
- **Path:** `/channels/:channelId/messages/:messageId/reactions/:emojiName/@me`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Create Reaction](https://docs.discord.com/developers/resources/message#create-reaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Discord channel ID. |
| `messageId` | path | `string` | yes | Discord message ID. |
| `emojiName` | path | `string` | yes | URL-encoded emoji identifier. |
