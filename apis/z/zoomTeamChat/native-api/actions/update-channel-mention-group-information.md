# Update Channel Mention Group Information with Zoom Team Chat

## Endpoint

- **Method:** `PATCH`
- **Path:** `/chat/channels/:channelId/mention_group/:mentionGroupId`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Update Channel Mention Group Information](https://developers.zoom.us/docs/api/rest/reference/chat/methods/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The channel ID. |
| `mentionGroupId` | path | `string` | yes | The mention group ID. |
| `name` | body | `string` | no | The updated mention group name. |
