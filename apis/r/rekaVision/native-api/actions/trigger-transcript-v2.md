# Trigger Transcript (V2) with Reka Vision

Creates a transcript generation job in Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/videos/:videoId/features/transcript`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Trigger Transcript (V2)](https://docs.reka.ai/vision/api-reference/v-2/trigger-transcript-v-2-videos-video-id-features-transcript-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `string` | yes | — |
| `force` | body | `boolean` | no | — |
| `chunking_config` | body | `object` | no | — |
| `chunking_config.min_len` | body | `number` | no | — |
| `chunking_config.max_len` | body | `number` | no | — |
| `chunking_config.use_scene_detection` | body | `boolean` | no | — |
| `chunking_config.use_asr` | body | `boolean` | no | — |
| `chunking_config.language` | body | `string` | no | — |
| `chunking_config.chunker_type` | body | `list<string>` | no | Accepted values: `max_utility`, `remote`. |
| `chunking_config.async_chunking` | body | `boolean` | no | — |
| `downsample_video` | body | `boolean` | no | — |
