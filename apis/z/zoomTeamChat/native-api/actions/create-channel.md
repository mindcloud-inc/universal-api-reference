# Create Channel with Zoom Team Chat

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/users/:userId/channels`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Create Channel](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/createChannel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user creating the channel. |
| `name` | body | `string` | yes | The channel name. |
