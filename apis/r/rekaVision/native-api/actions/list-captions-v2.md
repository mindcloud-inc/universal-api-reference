# List Captions (V2) with Reka Vision

Retrieves captions from Reka Vision.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/videos/:videoId/captions`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [List Captions (V2)](https://docs.reka.ai/vision/api-reference/v-2/list-captions-v-2-videos-video-id-captions-get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video_id` | path | `string` | yes |
| `start` | query | `number` | no |
| `end` | query | `number` | no |
| `page_limit` | query | `number` | no |
| `page_token` | query | `string` | no |
