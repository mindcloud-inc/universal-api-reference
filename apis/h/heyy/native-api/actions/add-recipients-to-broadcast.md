# Add Recipients To Broadcast with Heyy

Adds recipients to a broadcast in Heyy.

## Endpoint

- **Method:** `POST`
- **Path:** `/[:channelId]/broadcasts/:broadcastId/recipients`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Add Recipients To Broadcast](https://docs.heyy.io/api-reference/add-recipients-to-broadcast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcastId` | path | `string` | yes | The Heyy broadcast ID. |
| `channelId` | path | `string` | yes | The Heyy channel ID. |
| `contactsIds[]` | body | `array<string>` | yes | The contact IDs to add as recipients. |
