# List Scenes with Reka AI

Retrieves scenes from a Reka AI video.

## Endpoint

- **Method:** `GET`
- **Path:** `https://vision-agent.api.reka.ai/v2/videos/:video_id/scenes`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [List Scenes](https://docs.reka.ai/vision/api-reference/v-2/list-scenes-v-2-videos-video-id-scenes-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `string` | yes | The video identifier whose scenes to list. |
