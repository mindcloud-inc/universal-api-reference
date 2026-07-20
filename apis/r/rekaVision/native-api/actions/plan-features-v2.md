# Plan Features (V2) with Reka Vision

Retrieves feature planning results from Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/videos/:videoId/features/plan`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Plan Features (V2)](https://docs.reka.ai/vision/api-reference/v-2/plan-features-v-2-videos-video-id-features-plan-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video_id` | path | `string` | yes |
| `desired[]` | body | `array<string>` | yes |
