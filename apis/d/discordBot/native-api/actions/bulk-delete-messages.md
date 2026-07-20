# Bulk Delete Messages with Discord-Bot

Deletes multiple messages from a Discord channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:channelId/messages/bulk-delete`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Bulk Delete Messages](https://docs.discord.com/developers/resources/message#bulk-delete-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Discord channel ID. |
| `messages[]` | body | `array<string>` | yes | Message IDs to delete. |
