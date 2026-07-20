# Delete Broadcast with Heyy

Deletes an existing broadcast from a Heyy channel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/[:channelId]/broadcasts/:broadcastId`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Delete Broadcast](https://docs.heyy.io/api-reference/delete-broadcast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcastId` | path | `string` | yes | The Heyy broadcast ID. |
| `channelId` | path | `string` | yes | The Heyy channel ID. |
