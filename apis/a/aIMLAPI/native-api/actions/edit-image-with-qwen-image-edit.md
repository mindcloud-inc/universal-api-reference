# Edit Image With Qwen Image Edit with AI/ML API

Creates an edited image with Qwen Image Edit in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/generations`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Edit Image With Qwen Image Edit](https://docs.aimlapi.com/api-references/image-models/alibaba-cloud/qwen-image-edit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `image` | body | `string` | yes |
| `negative_prompt` | body | `string` | no |
| `prompt` | body | `string` | yes |
| `watermark` | body | `boolean` | no |
