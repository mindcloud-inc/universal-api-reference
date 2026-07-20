# Move Videos To Group (V2) with Reka Vision

Moves videos to a group in Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/video-groups/:groupId/videos`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Move Videos To Group (V2)](https://docs.reka.ai/vision/api-reference/v-2/move-videos-to-group-v-2-video-groups-group-id-videos-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group_id` | path | `string` | yes |
| `video_ids[]` | body | `array<string>` | yes |
