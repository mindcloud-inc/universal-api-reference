# Update Channel with Zoom Team Chat

## Endpoint

- **Method:** `PATCH`
- **Path:** `/chat/users/:userId/channels/:channelId`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Update Channel](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/updateChannel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user. |
| `channelId` | path | `string` | yes | The channel ID. |
| `name` | body | `string` | no | The updated channel name. |
