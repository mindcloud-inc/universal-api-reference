# Delete Own Reaction with Discord

Deletes the current user's reaction from a Discord message.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/channels/:channelId/messages/:messageId/reactions/:emojiName/@me`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Delete Own Reaction](https://docs.discord.com/developers/resources/message#delete-own-reaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | ID of the channel containing the message. |
| `messageId` | path | `string` | yes | ID of the message to remove reaction from. |
| `emojiName` | path | `string` | yes | Emoji to remove (URL-encoded as required by Discord). |
