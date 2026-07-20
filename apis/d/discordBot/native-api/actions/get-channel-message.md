# Get Channel Message with Discord-Bot

Retrieves a specific message from Discord.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:channelId/messages/:messageId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Get Channel Message](https://docs.discord.com/developers/resources/message#get-channel-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Discord channel ID. |
| `messageId` | path | `string` | yes | Discord message ID. |
