# Generate Image from Image (Legacy) with Dreamstudio

Creates a legacy image-to-image result in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/generation/:engine_id/image-to-image`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Generate Image from Image (Legacy)](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engine_id` | path | `string` | yes | DreamStudio engine identifier for the legacy text-to-image endpoint. |
| `init_image` | body | `file` | yes | Starting image file for the legacy image-to-image request. |
| `text_prompts[0][text]` | body | `string<object>` | yes | Prompt text for the legacy image-to-image request. |
| `init_image_mode` | body | `string` | no | Use IMAGE_STRENGTH or STEP_SCHEDULE to control how strongly the init image is preserved. |
| `image_strength` | body | `number` | no | How much the init image influences the output when init image mode is IMAGE_STRENGTH. |
