# Trigger Transcript with Reka AI

Triggers transcript generation for a video in Reka AI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://vision-agent.api.reka.ai/v2/videos/:video_id/features/transcript`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [Trigger Transcript](https://docs.reka.ai/vision/api-reference/v-2/trigger-transcript-v-2-videos-video-id-features-transcript-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `string` | yes | The video identifier to trigger transcript for. |
