# Bulk Delete Messages with Discord

Deletes multiple messages from a Discord channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:channelId/messages/bulk-delete`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Bulk Delete Messages](https://docs.discord.com/developers/resources/message#bulk-delete-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | ID of the channel containing the messages. |
| `messages[]` | body | `array<string>` | yes | List of message IDs to delete (2-100 IDs). |
| `filter_old` | body | `boolean` | no | When true, messages older than two weeks are filtered out instead of causing an error. |
