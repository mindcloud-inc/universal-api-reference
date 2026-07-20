# Extend Video with xAI

Extends a video in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/extensions`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Extend Video](https://docs.x.ai/developers/rest-api-reference/inference/videos#extend-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | no | Prompt describing the continuation. |
| `video` | body | `object` | no | Video object with a public MP4 URL. |
| `duration` | body | `number` | no | Extension duration in seconds. |
