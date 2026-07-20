# Create Sora 2 Image To Video Task with AI/ML API

Creates a Sora 2 image-to-video task in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/video/generations`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Create Sora 2 Image To Video Task](https://docs.aimlapi.com/api-references/video-models/openai/sora-2-i2v)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `aspect_ratio` | body | `string` | no |
| `duration` | body | `number` | no |
| `image_url` | body | `string` | yes |
| `prompt` | body | `string` | yes |
| `resolution` | body | `string` | no |
