# Submit Video-01 Generation with AI/ML API

Submits a Video-01 generation task in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/video/generations`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Submit Video-01 Generation](https://docs.aimlapi.com/api-references/video-models/minimax/video-01)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enhance_prompt` | body | `boolean` | no | Automatically optimize the prompt when helpful. |
| `image_url` | body | `string` | yes | A direct image URL or Base64-encoded image used as the first frame. |
| `prompt` | body | `string` | yes | — |
