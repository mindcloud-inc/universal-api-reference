# Edit Image With GPT Image 1 with AI/ML API

Creates an edited image with GPT Image 1 in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/edits`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Edit Image With GPT Image 1](https://docs.aimlapi.com/api-references/image-models/openai/gpt-image-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `image` | body | `file` | yes |
| `mask` | body | `file` | no |
| `prompt` | body | `string` | yes |
| `quality` | body | `string` | no |
| `size` | body | `string` | no |
