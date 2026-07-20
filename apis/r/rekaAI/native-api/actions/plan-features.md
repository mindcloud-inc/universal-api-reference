# Plan Features with Reka AI

Creates a feature plan in Reka AI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://vision-agent.api.reka.ai/v2/videos/:video_id/features/plan`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [Plan Features](https://docs.reka.ai/vision/api-reference/v-2/plan-features-v-2-videos-video-id-features-plan-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desired` | body | `string` | yes | Desired features to plan |
| `video_id` | path | `string` | yes | The video identifier to plan features for. |
