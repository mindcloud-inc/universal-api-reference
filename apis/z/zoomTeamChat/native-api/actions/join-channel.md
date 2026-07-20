# Join Channel with Zoom Team Chat

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/channels/:channelId/members/me`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Join Channel](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/joinChannel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The channel ID. |
