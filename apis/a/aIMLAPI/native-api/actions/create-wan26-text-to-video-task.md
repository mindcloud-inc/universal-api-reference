# Create Wan 2.6 Text To Video Task with AI/ML API

Creates a Wan 2.6 text-to-video task in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/video/generations`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Create Wan 2.6 Text To Video Task](https://docs.aimlapi.com/api-references/video-models/alibaba-cloud/wan-2.6-text-to-video)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `aspect_ratio` | body | `string` | no |
| `duration` | body | `number` | no |
| `enhance_prompt` | body | `boolean` | no |
| `generate_audio` | body | `boolean` | no |
| `negative_prompt` | body | `string` | no |
| `prompt` | body | `string` | yes |
| `resolution` | body | `string` | no |
