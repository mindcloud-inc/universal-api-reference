# Remove Recipients From Broadcast with Heyy

Removes recipients from a broadcast in Heyy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/[:channelId]/broadcasts/:broadcastId/recipients`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Remove Recipients From Broadcast](https://docs.heyy.io/api-reference/remove-recipients-from-broadcast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcastId` | path | `string` | yes | The Heyy broadcast ID. |
| `channelId` | path | `string` | yes | The Heyy channel ID. |
| `ids[]` | body | `array<string>` | yes | Recipient IDs to remove. |
