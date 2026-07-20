# List Objects (V2) with Reka Vision

Retrieves detected objects from Reka Vision.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/videos/:videoId/objects`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [List Objects (V2)](https://docs.reka.ai/vision/api-reference/v-2/list-objects-v-2-videos-video-id-objects-get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video_id` | path | `string` | yes |
| `start` | query | `number` | no |
| `end` | query | `number` | no |
| `type` | query | `string` | no |
| `page_limit` | query | `number` | no |
| `page_token` | query | `string` | no |
