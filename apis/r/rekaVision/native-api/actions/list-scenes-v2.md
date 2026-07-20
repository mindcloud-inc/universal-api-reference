# List Scenes (V2) with Reka Vision

Retrieves scenes from Reka Vision.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/videos/:videoId/scenes`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [List Scenes (V2)](https://docs.reka.ai/vision/api-reference/v-2/list-scenes-v-2-videos-video-id-scenes-get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video_id` | path | `string` | yes |
| `start` | query | `number` | no |
| `end` | query | `number` | no |
| `page_limit` | query | `number` | no |
| `page_token` | query | `string` | no |
