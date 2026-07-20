# Create Message with Discord-Bot

Creates a message in a Discord channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:channelId/messages`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Create Message](https://docs.discord.com/developers/resources/message#create-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Discord channel ID. |
| `content` | body | `string` | yes | Message contents, up to 2000 characters. |
