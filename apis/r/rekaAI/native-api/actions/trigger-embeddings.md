# Trigger Embeddings with Reka AI

Triggers embedding generation for a video in Reka AI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://vision-agent.api.reka.ai/v2/videos/:video_id/features/embeddings`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [Trigger Embeddings](https://docs.reka.ai/vision/api-reference/v-2/trigger-embeddings-v-2-videos-video-id-features-embeddings-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `string` | yes | The video identifier to trigger embeddings for. |
