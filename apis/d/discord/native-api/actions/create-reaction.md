# Create Reaction with Discord

Creates a reaction on a Discord message.

## Endpoint

- **Method:** `PUT`
- **Path:** `/channels/:channelId/messages/:messageId/reactions/:emojiName/@me`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Create Reaction](https://docs.discord.com/developers/resources/message#create-reaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | ID of the channel containing the message. |
| `messageId` | path | `string` | yes | ID of the message to react to. |
| `emojiName` | path | `string` | yes | Emoji to add as reaction (URL-encoded as required by Discord). |
