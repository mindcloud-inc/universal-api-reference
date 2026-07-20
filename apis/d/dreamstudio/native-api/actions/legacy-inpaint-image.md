# Legacy Inpaint Image with Dreamstudio

Creates a legacy inpainted image in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2alpha/generation/stable-image/inpaint`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Legacy Inpaint Image](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | body | `string` | no | Inpainting mode. Use search for prompt-driven masking or mask for explicit mask uploads. |
| `image` | body | `file` | yes | Source image file to inpaint. |
| `prompt` | body | `string` | yes | Prompt describing the edited result. |
| `search_prompt` | body | `string` | yes | Short description of what should be inpainted when mode is search. |
