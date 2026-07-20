# Get Channel with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/users/:userId/channels/:channelId`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Get Channel](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getChannel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user who is the member of the channel. |
| `channelId` | path | `string` | yes | The channel's unique identifier. |
