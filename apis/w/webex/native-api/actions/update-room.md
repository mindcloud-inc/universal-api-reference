# Update Room with Webex

Updates an existing room in Webex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/rooms/:roomId`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Update Room](https://developer.webex.com/messaging/docs/api/v1/rooms/update-a-room)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | yes | Room identifier. |
| `title` | body | `string` | yes | Updated room title. |
