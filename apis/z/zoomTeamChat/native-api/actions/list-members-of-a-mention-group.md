# List Members Of A Mention Group with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/channels/:channelId/mention_group/:mentionGroupId/members`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [List Members Of A Mention Group](https://developers.zoom.us/docs/api/rest/reference/chat/methods/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The channel ID. |
| `mentionGroupId` | path | `string` | yes | The mention group ID. |
