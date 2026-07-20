# List Captions with Reka AI

Retrieves captions from a Reka AI video.

## Endpoint

- **Method:** `GET`
- **Path:** `https://vision-agent.api.reka.ai/v2/videos/:video_id/captions`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [List Captions](https://docs.reka.ai/vision/api-reference/v-2/list-captions-v-2-videos-video-id-captions-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `string` | yes | The video identifier whose captions to list. |
