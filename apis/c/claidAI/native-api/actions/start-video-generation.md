# Start Video Generation with Claid AI

Starts a video generation job in Claid AI.

## Endpoint

- **Method:** `POST`
- **Path:** `video/generate`
- **Base URL:** `https://api.claid.ai/v1`
- **Official documentation:** [Start Video Generation](https://docs.claid.ai/image-to-video-api/async-api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input` | body | `string` | yes |
| `options` | body | `object` | yes |
| `output` | body | `string` | no |
