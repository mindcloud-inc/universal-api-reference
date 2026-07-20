# Start Broadcast with Heyy

Starts a broadcast in a Heyy channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/[:channelId]/broadcasts/:broadcastId/start`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Start Broadcast](https://docs.heyy.io/api-reference/start-broadcast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcastId` | path | `string` | yes | The Heyy broadcast ID. |
| `channelId` | path | `string` | yes | The Heyy channel ID. |
| `mediaId` | body | `string` | no | Optional media file ID. |
