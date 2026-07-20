# List Broadcast Recipients with Heyy

Retrieves broadcast recipients from a Heyy channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:channelId]/broadcasts/:broadcastId/recipients`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [List Broadcast Recipients](https://docs.heyy.io/api-reference/get-broadcast-recipients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcastId` | path | `string` | yes | The Heyy broadcast ID. |
| `channelId` | path | `string` | yes | The Heyy channel ID. |
