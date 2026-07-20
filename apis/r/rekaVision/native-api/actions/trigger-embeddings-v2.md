# Trigger Embeddings (V2) with Reka Vision

Creates an embedding job in Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/videos/:videoId/features/embeddings`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Trigger Embeddings (V2)](https://docs.reka.ai/vision/api-reference/v-2/trigger-embeddings-v-2-videos-video-id-features-embeddings-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video_id` | path | `string` | yes |
| `force` | body | `boolean` | no |
