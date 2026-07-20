# Leave Channel with Zoom Team Chat

## Endpoint

- **Method:** `DELETE`
- **Path:** `/chat/channels/:channelId/members/me`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Leave Channel](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/leaveChannel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The channel's unique identifier. |
