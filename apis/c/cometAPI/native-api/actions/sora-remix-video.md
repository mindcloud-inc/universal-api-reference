# Sora Remix Video with CometAPI

Creates a Sora video remix in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/videos/:video_id/remix`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Sora Remix Video](https://apidoc.cometapi.com/api/video/sora-2/official/remix-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Remix prompt. |
| `video_id` | path | `string` | yes | Video identifier. |
