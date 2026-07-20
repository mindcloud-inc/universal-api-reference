# List Channel Administrators with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/users/:userId/channels/:channelId/admins`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [List Channel Administrators](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/listChannelAdministrators)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user ID of member in the channel. |
| `channelId` | path | `string` | yes | The channel ID. |
