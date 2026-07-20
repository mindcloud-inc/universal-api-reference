# List Channel Members with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/users/:userId/channels/:channelId/members`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [List Channel Members](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/listChannelMembers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the channel owner or member. |
| `channelId` | path | `string` | yes | The channel ID. |
