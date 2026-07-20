# Create Channel Mention Group with Zoom Team Chat

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/channels/:channelId/mention_group`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Create Channel Mention Group](https://developers.zoom.us/docs/api/rest/reference/chat/methods/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The channel ID. |
| `name` | body | `string` | yes | The mention group name. |
