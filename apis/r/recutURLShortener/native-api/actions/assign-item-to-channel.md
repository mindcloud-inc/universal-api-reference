# Assign Item To Channel with Recut URL Shortener

Assigns an item to a channel in Recut URL Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/channel/:channelid/assign/:type/:itemid`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Assign Item To Channel](https://app.recut.in/developers#assign-an-item-to-a-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelid` | path | `number` | yes | Channel ID. |
| `type` | path | `string` | yes | Item type: `links`, `bio`, or `qr`. |
| `itemid` | path | `number` | yes | Item ID. |
