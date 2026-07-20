# Update Video Metadata (V2) with Reka Vision

Updates video metadata in Reka Vision.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/videos/:videoId`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Update Video Metadata (V2)](https://docs.reka.ai/vision/api-reference/v-2/update-video-metadata-v-2-videos-video-id-patch)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video_id` | path | `string` | yes |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
