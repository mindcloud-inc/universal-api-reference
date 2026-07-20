# Add Channel Members To A Mention Group with Zoom Team Chat

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/channels/:channelId/mention_group/:mentionGroupId/members`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Add Channel Members To A Mention Group](https://developers.zoom.us/docs/api/rest/reference/chat/methods/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The channel ID. |
| `mentionGroupId` | path | `string` | yes | The mention group ID. |
