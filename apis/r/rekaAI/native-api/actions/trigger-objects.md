# Trigger Objects with Reka AI

Triggers object detection for a video in Reka AI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://vision-agent.api.reka.ai/v2/videos/:video_id/features/objects`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [Trigger Objects](https://docs.reka.ai/vision/api-reference/v-2/trigger-objects-v-2-videos-video-id-features-objects-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `string` | yes | The video identifier to trigger objects for. |
