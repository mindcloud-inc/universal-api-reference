# Generate image prompt with 1minAI

Creates text prompts from uploaded images in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Generate image prompt](https://docs.1min.ai/docs/api/ai-for-image/image-to-prompt/image-to-prompt-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `imageUrl` | body | `string` | yes |
| `mode` | body | `string` | no |
| `n` | body | `number` | no |
