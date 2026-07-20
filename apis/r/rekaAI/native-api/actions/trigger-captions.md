# Trigger Captions with Reka AI

Triggers caption generation for a video in Reka AI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://vision-agent.api.reka.ai/v2/videos/:video_id/features/captions`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [Trigger Captions](https://docs.reka.ai/vision/api-reference/v-2/trigger-captions-v-2-videos-video-id-features-captions-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `string` | yes | The video identifier to trigger captions for. |
