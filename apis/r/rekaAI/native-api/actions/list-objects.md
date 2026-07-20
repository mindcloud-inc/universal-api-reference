# List Objects with Reka AI

Retrieves detected objects from a Reka AI video.

## Endpoint

- **Method:** `GET`
- **Path:** `https://vision-agent.api.reka.ai/v2/videos/:video_id/objects`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [List Objects](https://docs.reka.ai/vision/api-reference/v-2/list-objects-v-2-videos-video-id-objects-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `string` | yes | The video identifier whose objects to list. |
