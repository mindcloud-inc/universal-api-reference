# Trigger Captions (V2) with Reka Vision

Creates a captioning job in Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/videos/:videoId/features/captions`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Trigger Captions (V2)](https://docs.reka.ai/vision/api-reference/v-2/trigger-captions-v-2-videos-video-id-features-captions-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video_id` | path | `string` | yes |
| `force` | body | `boolean` | no |
| `caption_prompt` | body | `string` | no |
