# List User's Channels with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/users/:userId/channels`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [List User's Channels](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getChannels)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user. |
