# Delete Message with Discord-Bot

Deletes a message from a Discord channel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/channels/:channelId/messages/:messageId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Delete Message](https://docs.discord.com/developers/resources/message#delete-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Discord channel ID. |
| `messageId` | path | `string` | yes | Discord message ID. |
