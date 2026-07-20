# Create Sora 2 Text To Video Task with AI/ML API

Creates a Sora 2 text-to-video task in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/video/generations`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Create Sora 2 Text To Video Task](https://docs.aimlapi.com/api-references/video-models/openai/sora-2-t2v)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `aspect_ratio` | body | `string` | no |
| `duration` | body | `number` | no |
| `prompt` | body | `string` | yes |
| `resolution` | body | `string` | no |
