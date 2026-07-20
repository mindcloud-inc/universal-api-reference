# Assign Item to Channel with JmpTo

Assigns an item to a channel in JmpTo.

## Endpoint

- **Method:** `POST`
- **Path:** `/channel/:channelid/assign/:type/:itemid`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Assign Item to Channel](https://jmpto.net/developers#assign-an-item-to-a-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelid` | path | `number` | yes | Channel ID to assign the item to. |
| `type` | path | `string` | yes | Item type to assign to the channel. |
| `itemid` | path | `number` | yes | Item ID to assign to the channel. |
