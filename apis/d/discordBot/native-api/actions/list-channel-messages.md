# List Channel Messages with Discord-Bot

Retrieves messages from a Discord channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:channelId/messages`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [List Channel Messages](https://docs.discord.com/developers/resources/message#get-channel-messages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return messages after this message ID. |
| `around` | query | `string` | no | Return messages around this message ID. Do not combine with before or after. |
| `channelId` | path | `string` | yes | Discord channel ID. |
