# List Transcript (V2) with Reka Vision

Retrieves transcript data from Reka Vision.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/videos/:videoId/transcript`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [List Transcript (V2)](https://docs.reka.ai/vision/api-reference/v-2/list-transcript-v-2-videos-video-id-transcript-get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video_id` | path | `string` | yes |
| `start` | query | `number` | no |
| `end` | query | `number` | no |
| `format` | query | `string` | no |
| `page_limit` | query | `number` | no |
| `page_token` | query | `string` | no |
