# List Messages with Discord

Lists messages in a Discord channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:channelId/messages`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [List Messages](https://docs.discord.com/developers/resources/message#get-channel-messages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel identifier. |
| `limit` | query | `number` | no | Maximum number of messages to return (1-100). |
| `around` | query | `string` | no | Get messages around this message ID. |
| `before` | query | `string` | no | Get messages before this message ID. |
| `after` | query | `string` | no | Get messages after this message ID. |
