# Get Broadcast by ID with Heyy

Retrieves a broadcast by ID from Heyy.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:channelId]/broadcasts/:broadcastId`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Get Broadcast by ID](https://docs.heyy.io/api-reference/get-broadcast-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcastId` | path | `string` | yes | The Heyy broadcast ID. |
| `channelId` | path | `string` | yes | The Heyy channel ID. |
